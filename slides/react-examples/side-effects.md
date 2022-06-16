---
layout: two-cols
---

::default::

## Vue

Component:

```tsx
<template>
  <div>
    <div v-if="user">
      <div>Username: {{ user.name }}</div>
      <div>Email: {{ user.email }}</div>
    </div>
    <div v-else>Fallback</div>
  </div>
</template>

<script lang="ts">
export default {
  props: {
    userId: {
      type: String
    }
  },
  data(): { user: User | null } {
    return { user: null }
  },
  async mounted() {
    this.user = await this.fetchUser(this.props.userId);
  },
  watch: {
    async userId(newId: string) {
      this.user = await this.fetchUser(newId);
    },
  },
  methods: {
    fetchUser(userId: string) {
      return MyAPI.getUser(userId);
    }
  }
}
</script>
```

::right::

<v-click>

## React

Component:

```tsx
interface Props {
  userId: string;
}

export function UserProfile({ userId }: Props) {
  const [user, userId] = useState<User | null>(null);

  useEffect(() => {
    MyAPI.getUser(userId).then(setUser);
  }, [userId]);

  if (!user) {
    return <div>Fallback</div>;
  }

  return (
    <div>
      <div>Username: {user.name}</div>
      <div>Email: {user.email}</div>
    </div>
  );
}
```

</v-click>