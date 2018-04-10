<template>
    <div class="container">
        <div class="row">
            <div class="col-xs-12">
                <app-quote>
                <h2>{{ quoteTitle }}</h2>
                <p>An amazing quote</p>
                </app-quote>
            </div>
        </div>
    </div>
</template>

<script>
import appQuote from './components/Quote.vue';

export default {
    data: function() {
        return {
            quoteTitle: 'The Quote',
        };
    },
    components: {
        appQuote,
    },
};
</script>

<style>
</style>
