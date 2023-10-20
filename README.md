<h1>Przydatne skrypty</h1>
<h2> Sprawdzanie wysokośći elementu</h2
<pre>
    ref="calendar"
    <br/>
    function getHeight() {
    const currentHeight = calendar.value?.$el.clientHeight;
    calendarStore.setCalendarHeight(currentHeight);
}

window.addEventListener("resize", getHeight);
</pre>

<h2> Reagowanie na koniec skrolu</h2
<pre>
        @scroll="loadMoreOnScrollEnd"<br/>
const loadMoreOnScrollEnd = (event: Event) => {
<br/>
    const target = event.target as HTMLElement;
<br/>
    if (target.scrollTop + target.clientHeight >= target.scrollHeight) {
       console.log('end');
<br/>
    }
<br/>
};
</pre>

<h2> Skrypt do Vuetify composition api(helpers)</h2
<pre>
import {getCurrentInstance} from 'vue';
export const useVuetify = () => {    
    const vm = getCurrentInstance();
    return vm?.proxy?.$vuetify || null;
};
</pre>
