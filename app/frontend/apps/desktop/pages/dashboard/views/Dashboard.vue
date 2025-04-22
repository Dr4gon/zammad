<!-- Copyright (C) 2012-2025 Zammad Foundation, https://zammad-foundation.org/ -->

<script setup lang="ts">
import { reactive } from 'vue'

import { useSessionStore } from '#shared/stores/session.ts'

import CommonSimpleTable from '#desktop/components/CommonTable/CommonSimpleTable.vue'
import LayoutMain from '#desktop/components/layout/LayoutMain.vue'

const session = useSessionStore()

const tableHeaders = [
  {
    key: 'name',
    label: 'User name',
  },
  {
    key: 'title',
    label: 'Job position',
    truncate: true,
  },
  {
    key: 'email',
    label: 'Email',
  },
  {
    key: 'role',
    label: 'Role',
  },
]

const tableItems = reactive([
  {
    id: 1,
    name: 'Lindsay Walton',
    title: 'Front-end Developer',
    email: 'lindsay.walton@example.com',
    role: 'Member',
    checked: true,
  },
  {
    id: 2,
    name: 'Courtney Henry',
    title: 'Designer',
    email: 'courtney.henry@example.com',
    role: 'Admin',
  },
  {
    id: 3,
    name: 'Tom Cook',
    title: 'Director of Product',
    email: 'tom.cook@example.com',
    role: 'Member',
  },
  {
    id: 4,
    name: 'Whitney Francis',
    title: 'Copywriter',
    email: 'whitney.francis@example.com',
    role: 'Admin',
  },
  {
    id: 5,
    name: 'Leonard Krasner',
    title: 'Senior Designer Principal Designer ',
    email: 'leonard.krasner@example.com',
    role: 'Owner',
  },
  {
    id: 6,
    name: 'Floyd Miles',
    title:
      'Principal Designer for a very long way to go to see the end of the title. It is a very long title, indeed.',
    email: 'floyd.miles@example.com',
    role: 'Member',
  },
  {
    id: 7,
    name: 'Floyd Miles2',
    title:
      'Principal Designer for a very long way to go to see the end of the title. It is a very long title, indeed.',
    email: 'floyd.miles@example.com',
    role: 'Member',
  },
  {
    id: 8,
    name: 'Floyd Miles3',
    title:
      'Principal Designer for a very long way to go to see the end of the title. It is a very long title, indeed.',
    email: 'floyd.miles@example.com',
    role: 'Member',
  },
  {
    id: 9,
    name: 'Floyd Miles4',
    title:
      'Principal Designer for a very long way to go to see the end of the title. It is a very long title, indeed.',
    email: 'floyd.miles@example.com',
    role: 'Member',
  },
  {
    id: 10,
    name: 'Floyd Miles5',
    title:
      'Principal Designer for a very long way to go to see the end of the title. It is a very long title, indeed.',
    email: 'floyd.miles@example.com',
    role: 'Member',
  },
])
</script>

<template>
  <LayoutMain>
    Hello, {{ session.user?.fullname }}!

    <!-- TODO: content -->
    <h2 class="mt-8 mb-2">All tickets created by today</h2>
    <div class="mb-6 flex flex-col gap-4">
      <CommonSimpleTable
        caption="test"
        :headers="tableHeaders"
        :items="tableItems"
      ></CommonSimpleTable>
    </div>
  </LayoutMain>
</template>
