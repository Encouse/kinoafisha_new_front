
import { Component, Prop, Vue } from "vue-property-decorator"
import Axios, { AxiosResponse } from "axios"
import { BriefFilm } from "@/film-model"
import { getFilmById } from "@/api/film"


export default class FilmView extends Vue {
    private filmEntity!: FilmModel
    private dataReady = false
    async mounted() {
        this.filmEntity = await getListOfFilms()
        this.dataReady = true
    }
}
