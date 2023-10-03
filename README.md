Sprawdzanie wysokośći elementu

-function getHeight() {
    const currentHeight = calendar.value?.$el.clientHeight;
    calendarStore.setCalendarHeight(currentHeight);
}

window.addEventListener("resize", getHeight);


Reagowanie na koniec skrolu
- @scroll="loadMoreOnScrollEnd"
- const loadMoreOnScrollEnd = (event: Event) => {
    const target = event.target as HTMLElement;
    if (target.scrollTop + target.clientHeight >= target.scrollHeight) {
       console.log('end');
    }
};
