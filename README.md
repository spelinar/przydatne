# Przydatne skrypty
## Sprawdzanie wysokośći elementu
```js
    ref="calendar"
    function getHeight() {
    const currentHeight = calendarRef.value?.clientHeight;
    calendarStore.setCalendarHeight(currentHeight); -> zapis do storege aby można było użyć w innych komponentach
    window.addEventListener("resize", getHeight); -> służy do zmiany dynamicznej rozmiaru
}
```
## Reagowanie na koniec skrolu
```js
        @scroll="loadMoreOnScrollEnd"<br/>
const loadMoreOnScrollEnd = (event: Event) => {
    const target = event.target as HTMLElement;
    if (target.scrollTop + target.clientHeight >= target.scrollHeight) {
       console.log('end');
    }
};
```

## Skrypt do Vuetify composition api(helpers)
```js
import {getCurrentInstance} from 'vue';
export const useVuetify = () => { 
    const vm = getCurrentInstance();
    return vm?.proxy?.$vuetify || null;
};
```

## Musimy owinąć w v-row i w v-rowie dodać :style="height: height + 'px'"
```js
const height = computed(() => {
    return vuetify?.breakpoint.height;
})
```
