<template>
    <div class="contact">
        <h1>Contact Us</h1>
        <form @submit.prevent="subForm">
            <label for="fname">Full Name: </label>
            <input type="text" id="fname" required v-model="fullname">
            <div v-if="nameError" class="error">{{ nameError }}</div>
            <label for="myemail">Email: </label>
            <input type="email" id="myemail" required v-model="email">
            <div v-if="emailError" class="error">{{ emailError }}</div>
            <label for="comments">Questions or comments: </label>
            <textarea id="comments" name="comments" rows="3" cols="48" required v-model="comments"></textarea>
            <div v-if="commentsError" class="error">{{ commentsError }}</div>
            <div class="btn">
                <button>Submit</button>
            </div>
        </form>
        <div v-if="showReceipt" class="receipt">
            <h3>Confirmation</h3>
            <p>Your full name: {{ fullname }}</p>
            <p>This is the email you typed: {{ email }}</p>
            <p>The questions or comments received is: {{ comments }}</p>
        </div>
    </div>
</template>
<script>
export default {
    data() {
        return {
            fullname: '',
            nameError: '',
            email: '',
            emailError: '',
            comments: '',
            commentsError: '',
            showReceipt: false
        }
    },
    methods: {
        subForm() {
            this.nameError = this.fullname.length >= 10 ? '' : 'Your full name must have at least 10 characters';
            this.commentsError = this.comments.length >= 3 ? '' : 'Your questions or comments must have at least 3 characters';
            var validRegex = /^[a-zA-Z0-9.!#$%&'*+/=?^_`{|}~-]+@[a-zA-Z0-9-]+(?:\.[a-zA-Z0-9-]+)*$/;
            this.emailError = this.email.match(validRegex)? '' : 'Your email address must be valid';
            if (!this.emailError && !this.nameError && !this.commentsError) {
                this.showReceipt = true
            } else {
                this.showReceipt = false
            }
        }
    }
}
</script>
<style>
.contact {
    padding: 1rem;
    background-color: azure;
}
form {
    max-width: 400px;
    margin: 20px auto;
    background-color: azure;
    text-align: left;
}

input, select {
    display: block;
    width: 100%;
    color: #333;
    padding: 5px;
    box-sizing: border-box;
    border-bottom: 1px solid lightcyan;
}

label {
    display: inline-block;
    margin: 20px 0;
    color: #777;
    font-weight: bold;
}

input[type="checkbox"] {
    width: 20px;
    display: inline-block;
    margin-right: 15px;
}
.btn {
    text-align:center;
}
button {
    padding: 5px;
    margin-top: 10px;
    border-radius: 10px;
}
.error {
    color: red;
    font-size: 0.7em;
    font-style: italic;
}

.receipt {
    background-color: white;
    margin: auto;
}
</style>