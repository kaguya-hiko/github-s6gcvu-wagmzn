<template>
  <div>
    <h1>MEMBER</h1>
    <p>member紹介</p>
    <ul>
      <li v-for="user in users">
        名前:{{ user.name }}<br />出身:{{ user.pref }} {{ user.city }}
        <br />
        <img src="user.photo," alt="user.name" />
        {{ user.photo }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  async setup() {
    const { data: users } = await useFetch('/api/users');
    return { users };
  },
};
</script>
