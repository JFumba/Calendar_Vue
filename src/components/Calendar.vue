<template>
    <article id="calendar">
        <header>
            <div class="current-date">
                <div class="current-day">
                    Saturday
                </div>
                <div class="today">
                    <div><div class="arrow-up"></div></div>
                    <div><div class="arrow-up"></div></div>
                    <div><div class="arrow-up"></div></div>
                    <div>10</div>
                    <div>August</div>
                    <div>2019</div>
                    <div><div class="arrow-down"></div></div>
                    <div><div class="arrow-down"></div></div>
                    <div><div class="arrow-down"></div></div>
                </div>
            </div>
        </header>
        <section>
            <div class="weekdays">
                <div class="weekday" v-for="(weekday, index) in weekdays" :key="index">
                    {{ weekday }}
                </div>
            </div>
            <div class="date">
                <div class="day-hidden">29</div>
                <div class="day-hidden">30</div>
                <div class="day-hidden">31</div>
                <div class="day" v-for="(n, index) in 31" :key="index" >
                    {{ n }}
                </div>
                <div class="day-hidden" v-for="(n, index) in 8" :key="index" >
                    {{ n }}
                </div>
            </div>
        </section>
    </article>
</template>

<script>
export default {
    data: function() {
        return {
            weekdays: ['Mo', 'Tu', 'We', 'Th', 'Fr', 'Sa', 'Su'],
        }
    }
}
</script>

<style lang="scss" scoped>
    @import url('https://fonts.googleapis.com/css?family=Anton');
    #calendar {
        width: 460px;
        height: 730px;
        background-color: #efefef;
        font-family: 'Anton';
        border-radius: 15px;
        overflow: hidden;
    }
</style>