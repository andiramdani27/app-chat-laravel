<template>
    <div class="chat-lists">
    	<div class="messages">
    		<div class="user">Andi Ramdani
    			<span class="time">22/11/2019 05:00</span>
    		</div>
    		<div class="message">
    			ini contoh chat saya
    		</div>

            <hr>

    		<div class="user">Yani Nurmayani
    			<span class="time">23/11/2019 14:00</span>
    		</div>
    		<div class="message">
    			ini contoh chat yani
    		</div>
    	</div>
    </div>
</template>

<script>
    export default {
        mounted() {
            console.log('Component mounted.')
        }
    }
</script>

<style lang="scss">
    .messages {
        margin-top: 5px;
    }

    .time {
        font-weight: 800;
    }

    .message {
        font-size: 2rem;
    }    
</style>
