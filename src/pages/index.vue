<script setup>
import Card from '../components/Card.vue'

const list = [
  {
    "id": 1,
    "name": "John Doe",
    "occupation": "Software Engineer",
    "company": "ABC Tech",
    "email": "john.doe@example.com",
    "phone": "+1 (555) 123-4567",
    "address": {
      "street": "123 Main St",
      "city": "Anytown",
      "state": "CA",
      "zip": "12345",
      "country": "USA"
    }
  },
  {
    "id": 2,
    "name": "Jane Smith",
    "occupation": "Graphic Designer",
    "company": "Design Co.",
    "email": "jane.smith@example.com",
    "phone": "+1 (555) 987-6543",
    "address": {
      "street": "456 Elm St",
      "city": "Somewhere",
      "state": "NY",
      "zip": "54321",
      "country": "USA"
    }
  },
  {
    "id": 3,
    "name": "Alice Johnson",
    "occupation": "Marketing Manager",
    "company": "Marketing Pro",
    "email": "alice.johnson@example.com",
    "phone": "+1 (555) 567-8901",
    "address": {
      "street": "789 Oak St",
      "city": "Nowhere",
      "state": "TX",
      "zip": "67890",
      "country": "USA"
    }
  }
]

</script>

<template>
<section>
  <table class=" table-auto w-full">
    <caption class="font-bold text-2xl/loose">用v-bind功能</caption>
    <thead>
      <tr class=" bg-indigo-400">
        <th>Name</th>
        <th>occupation</th>
        <th>email</th>
      </tr>
    </thead>
    <tbody>
      <tr class=" bg-indigo-100 odd:bg-indigo-50" v-for="item in list">
        <Card v-bind="item" />
      </tr>
    </tbody>
  </table>
</section>
</template>
