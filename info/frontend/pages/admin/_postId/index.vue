<template>
  <newPostFrom
    :postEdit="post"
    @submit="onSubmit" />
</template>

<script>
import newPostFrom from '@/components/Admin/NewPostFrom.vue'
export default {
  components: { newPostFrom },
  layout: 'admin',
  data () {
    return {
      post: {
        id: 1,
        title: '1 post',
        descr: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit',
        content: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Lorem ipsum dolor sit amet, consectetur adipiscing elit',
        img: 'https://lawnuk.com/wp-content/uploads/2016/08/sprogs-dogs.jpg'
      },
    }
  },
  methods: {
    onSubmit (post) {
      console.log('Post Editing!')
      console.log(post)
    }
  }
}
</script>
