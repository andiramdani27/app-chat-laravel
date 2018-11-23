<template>
    <div class="chat-lists">
    	<div class="messages" v-for="message in messages">
    		<div class="user">{{ message.user.name }} -
    			<span class="time">{{ message.created_at }}</span>
    		</div>
    		<div class="message">
    			{{ message.subject }}
    		</div>
            <hr>
    	</div>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                messages:[]
            }
        },
        mounted() {
            this.getMessage();
        },
        methods: {
            getMessage() {
                axios.get('/messages').then(response => {
                    this.messages = response.data
                });
            }
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
        font-size: 1.5rem;
    }
    .chat-lists {
        max-height:400px;
        overflow-y:scroll;
    }
</style>
