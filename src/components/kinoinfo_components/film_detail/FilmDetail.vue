<template>
  <div class = 'poster-block'>


          <ActionPosterImage
          v-if = "obj"
          :kid = 'obj.kid'
          :limit = 'obj.limits'
          :title = 'obj.name[0].name'
          :rate = 'obj.imdb_rate'
          :description = 'obj.description'
          :persons = 'obj.persons'
          :likes = 'obj.votes.likes'
          :dislikes = 'obj.votes.dislikes'
          :year = 'obj.year'
          :country = 'obj.country'
          :votes = 'obj.imdb_votes'
          :release = 'obj.release'
          :genre = 'obj.genre'
          :id = 'obj.id'
          />

  </div>
</template>

<script>
// Страница с детальным вывоом информации о фильме
// На данный момент просто принимает id фильма из роутера
// и рендерит компонент ActionPosterImage0, оборачивая его в доп. блок
  import ActionPosterImage from "@/components/kinoinfo_components/action_poster/ActionPosterImage.vue"
  export default {
    name: 'filmdetail',
    components: {
      ActionPosterImage,
    },
    //obj received from CHAIN |- FIlmDetailView => FilmDetail => FilmPoster
    props: {
      obj: Object,
    },

}

</script>

<style scoped lang='scss'>
.poster-block {
  width: 100%;
  height: 100%;
}

</style>
