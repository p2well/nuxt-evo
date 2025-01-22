<template>
  <UContainer>
    <UCard class="mt-10" role="region" aria-labelledby="page-title">
      <template #header>
        <div class="flex justify-between">
          <h1 id="page-title">Users</h1>
          <UBadge color="primary" variant="solid"
            >Total: {{ totalCount }}</UBadge
          >
        </div>
      </template>
      <div
        class="flex justify-between border-b items-center w-full px-4 py-3 border-gray-200 dark:border-gray-700"
      >
        <div class="flex items-center gap-1.5">
          <span class="text-sm leading-5">Rows per page:</span>

          <USelect
            v-model="pageCount"
            :options="[5, 10, 20]"
            class="me-2 w-20"
            size="xs"
          />
        </div>
      </div>
      <UTable
        :loading="loading"
        :loading-state="{
          icon: 'i-heroicons-arrow-path-20-solid',
          label: 'Loading...',
        }"
        :progress="{ color: 'primary', animation: 'carousel' }"
        class="w-full"
        :columns="columns"
        :rows="pageRows"
      />
      <template #footer>
        <div class="flex flex-wrap justify-between items-center">
          <div>
            <span class="text-sm leading-5">
              Showing
              <span class="font-medium">{{ pageFrom }}</span>
              to
              <span class="font-medium">{{ pageTo }}</span>
              of
              <span class="font-medium">{{ totalCount }}</span>
              results
            </span>
          </div>
          <UPagination
            v-model="page"
            :page-count="pageCount"
            :total="totalCount"
          />
        </div>
      </template>
    </UCard>
  </UContainer>
</template>

<script setup lang="ts">
// Define types
interface Column {
  key: string;
  label: string;
  sortable: boolean;
}

interface Row {
  id: string;
  name: string;
  title: string;
  email: string;
  role: string;
}

interface FetchedData {
  columns: Column[];
  rows: Row[];
  totalCount: number;
}

// Use types in refs
const loading = ref(true);
const columns = ref<Column[]>([{ key: '', label: '', sortable: false }]);
const rows = ref<Row[]>([]);
const totalCount = ref<number>(0);
const page = ref(1);
const pageCount = ref(5);
const pageFrom = computed(() => (page.value - 1) * pageCount.value + 1);
const pageTo = computed(() =>
  Math.min(page.value * pageCount.value, totalCount.value)
);
const pageRows = computed(() => {
  return rows.value.slice(
    (page.value - 1) * pageCount.value,
    page.value * pageCount.value
  );
});

const fetchApiData = async () => {
  loading.value = true;

  const { data: fetchedData } = await useFetch<FetchedData>('/api/users', {
    params: {},
  });

  if (fetchedData.value) {
    columns.value = fetchedData.value.columns;
    rows.value.push(...fetchedData.value.rows);
    totalCount.value = fetchedData.value.totalCount;
  }

  loading.value = false;
};

fetchApiData();
</script>
