<template>
    <div>
        <RequestItem v-for="request in requests" :key="request.id" :request="request" />
    </div>
</template>

<script>
import RequestItem from './RequestItem.vue';

export default {
    name: "RequestList",
    components: {
        RequestItem
    },
    data() {
        return {
            requests: [
                {
                    id: 1,
                    name: "Fingerbot Housing for Electric Radiator",
                    description: "Housing and lever for automating an electric radiator.",
                    status: false,
                    link: "https://cad.onshape.com/documents/b8ec8801d0b731e6343332f0/w/f4d5bcb29b2722765cb6d062/e/e1db267c73200326b538a737?renderMode=0&uiState=67320b1eae1f23679ee2c218"
                },
                {
                    id: 2,
                    name: "Cardboard Box Handle",
                    description: "2-part handle to make cardboard box handles more sturdy.",
                    status: true,
                    link: "https://cad.onshape.com/documents/71abd6fc3ce6fed7e6a05485/w/368905de720fe40a577fe632/e/d8a57b8590b4a5671c514ffa?renderMode=0&uiState=6729e07989212b582ec5eacb"
                }
            ]
        };
    }
};
</script>