<template>
    <Card>
        <form>
            <h2>
                How would you rate your service with us?
            </h2>
            <!-- Rating Component -->
            <rating-select 
                :rating="rating" 
                @setRating="setRating" />
            <div class="input-group">
                <input 
                    type="text"
                    placeholder="Write a review"
                    v-model="text"
                >
                <button
                    type="submit"
                    class="btn btn-primary"
                    :disabled="btnDisabled"
                >
                </button>
                
            </div>
            <div class="message">
                Text must be at least 10 charcters.
            </div>
        </form>
    </Card>
</template>

<script setup>
    import { ref } from 'vue';
    import Card from './shared/Card.vue';
    import RatingSelect from './RatingSelect.vue';
    const text = ref('');
    const btnDisabled = ref(false);
    const message = ref("");
    const rating = ref(9);

    const setRating = (val) => {
        rating.value = val;
        console.log(val);
    }
</script>

<style>

</style>