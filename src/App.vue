<template>
    <div class="container">
        <div class="row">
            <div class="col-xs-12">
                <hr>
                <button @click="selectedComponent = 'appQuote'">Quote</button>
                <button @click="selectedComponent = 'appAuthor'">Author</button>
                <button @click="selectedComponent = 'appNew'">New</button>
                <hr>
                <p>{{ selectedComponent }}</p>
                <keep-alive>
                    <component :is="selectedComponent">
                        <p>Default Content</p>
                    </component>
                </keep-alive>

                <!-- <app-quote>
                <h2 slot="title">{{ quoteTitle }}</h2>
                <p>An amazing quote</p>
                </app-quote> -->
            </div>
        </div>
    </div>
</template>

<script>
import appQuote from './components/Quote.vue';
import appAuthor from './components/Author.vue';
import appNew from './components/New.vue';

export default {
    data: function() {
        return {
            quoteTitle: 'The Quote',
            selectedComponent: 'appQuote',
        };
    },
    components: {
        appQuote,
        appAuthor,
        appNew,
    },
};
</script>

<style>
</style>
