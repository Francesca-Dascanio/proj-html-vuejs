<script>

export default {
    name: 'AppModal',
    data () {
        return {
            button: false,
            inputName: '',
            inputLastName: '',

        }
    },
    methods: {
        getConfirmation: function () {

            const selectService = document.getElementById('services');
            console.log(selectService);

            const selectBarbers = document.getElementById('barbers');

            if ((selectService.value == '') || (selectBarbers.value == '') || (this.inputName == '') || (this.inputLastName == '')) {
                alert('Fill the form before submitting!');
            }
            else {
                alert('Appointment has been booked successfully!');
            }
            
        }
    }
}

</script>

<template>
     <div class="modal"
     :class="{
        'visible': button == false,
        'not-visible': button == true
     }">
        <div class="title-container flex space-btw">
            <h3>
                Book your appointment
            </h3>
            <div class="exit" @click="$emit('getOff')">
                <font-awesome-icon icon="fa-solid fa-xmark" size="xl" />
            </div>
        </div>
        <hr>
        <form action="">
            <label for="services">Select a Service:</label>
                <select name="services" id="services" required>
                    <option value=""> -- Select -- </option>
                    <option value="trim">Trim & Cut</option>
                    <option value="wash">Wash & Dry</option>
                    <option value="beard">Beard Tidy</option>
                </select>
            <label for="barbers">Select your Barber:</label>
                <select name="barbers" id="barbers" required>
                    <option value=""> -- Select -- </option>
                    <option value="michael">Michael</option>
                    <option value="jim">Jim</option>
                    <option value="dwight">Dwight</option>
                    <option value="creed">Creed</option>
                </select>
            <label for="start">Select a Day:</label>
                <input type="date" id="day" name="trip-start" required
                value="2023-03-01"
                min="2023-02-16" max="2023-12-31">
            <label for="name">First Name:</label>
                <input type="text" id="name" name="name" required v-model="inputName"
                minlength="4" maxlength="20">
            <label for="name">Last Name:</label>
                <input type="text" id="name" name="name" required v-model="inputLastName"
                minlength="4" maxlength="20">
            <button type="submit" @click="getConfirmation()">
                Save & Book
            </button>  
        </form>
    </div>
</template>

<style lang="scss" scoped>
@import '../styles/partials/variables.scss';
@import '../styles/partials/mixins.scss';

.modal {
    position: absolute;
    top: 50%;
    left: 50%;
    width: 50%;
    color: $sixth-color;
    transform: translate(-50%,-50%);
    background-color: $third-color;
    border-radius: 5px;

    .title-container {
        padding: 1rem;
    }

    form {
        padding: 1rem;

        label {
            margin: 0.5rem 0;
            display: block;
        }

        select, input {
            width: 50%;
            display: block;
        }

        button {
            @include button ($third-color);
            margin: 1rem 0;
        }
    }
}

.message {
    position: absolute;
    top: 50%;
    left: 50%;
    width: 50%;
    color: $sixth-color;
    transform: translate(-50%,-50%);
    background-color: $third-color;
    border-radius: 5px;
    padding: 2rem;
    color: $third-color;
    background-color: $primary-color;
}

</style>
