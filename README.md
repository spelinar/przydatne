<h1>Przydatne skrypty</h1>
<h2> Sprawdzanie wysokośći elementu</h2
<pre>function getHeight() {
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
