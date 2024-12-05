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
                    shortDescription: "Housing and lever to automate radiator controls.",
                    longDescription: `
<strong>3D Printing Factory Order Slip</strong><br>
<strong>Client:</strong> Nejc Kovačič<br>
<strong>Order ID:</strong> FRH-2024-003<br><br>

<strong>Item Details:</strong><br>
<strong>Product Name:</strong> Fingerbot Housing for Electric Radiator Automation<br>
<strong>Parts:</strong> 2 (1 Housing, 1 Lever)<br>
<strong>Material:</strong> Sturdy PLA (suggested, open to feedback)<br>
<strong>Color:</strong> Preferably white or closest available shade 🎨<br>
<strong>Function:</strong> Housing for a fingerbot-style device to automate an electric radiator. Practicality over beauty!<br><br>

<strong>Production Specifications:</strong><br>
- Quantity: 1 set (1 housing, 1 lever)<br>
- Visual Quality: Heads up: This might be an "unconventionally stylish" (aka ugly) print. All charm lies in the function.<br>
- Heaviness: This design may be on the heavier side. Please check for print feasibility and let me know if modifications are required to lighten it.<br>
- Design Export: Accessible via this link for your expert printing skills<br>
<a href="https://cad.onshape.com/documents/b8ec8801d0b731e6343332f0/w/f4d5bcb29b2722765cb6d062/e/e1db267c73200326b538a737?renderMode=0&uiState=67320b1eae1f23679ee2c218" target="_blank">View Design</a><br><br>

<strong>Quality Control and Feedback:</strong><br>
- Fit and Function: Ensure smooth functionality of the lever and general tolerances.<br>
- Feedback Needed: Please provide feedback on the aesthetics or structure. If it looks like a beast or feels too heavy, I’m ready to make design changes.<br><br>

<strong>Production Timeline:</strong> Prototype Requested: Whenever you can work some magic! ✨<br><br>

<strong>Note:</strong> Beauty is optional, but automation is essential for this project!
`,
                    status: true,
                    link: "https://cad.onshape.com/documents/b8ec8801d0b731e6343332f0/w/f4d5bcb29b2722765cb6d062/e/e1db267c73200326b538a737?renderMode=0&uiState=67320b1eae1f23679ee2c218",
                    date: "2024-11-10"
                },
                {
                    id: 2,
                    name: "Cardboard Box Handle",
                    description: "2-part handle designed to reinforce cardboard box handles for improved durability and easier carrying.",
                    shortDescription: "Reinforces cardboard box handles with a clip-on mechanism.",
                    longDescription: `
<strong>3D Printing Factory Order Slip</strong><br>
<strong>Client:</strong> Nejc Kovačič<br>
<strong>Order ID:</strong> CBH-2024-001<br><br>

<strong>Item Details:</strong><br>
<strong>Product Name:</strong> Cardboard Box Handle<br>
<strong>Parts:</strong> 2-part handle (clips together)<br>
<strong>Material:</strong> Standard PLA (unless otherwise specified by Factory)<br>
<strong>Color:</strong> Surprise me! 🌈<br>
<strong>Function:</strong> Reinforcement handle for cardboard boxes (1 handle per box)<br><br>

<strong>Production Specifications:</strong><br>
- Quantity: 1 test print initially (total order: 4 handles across 4 boxes)<br>
- Assembly Check: Ensure easy clip-together mechanism. No glue, tape, or magic spells should be required.<br>
- Design Export: Accessible via the following URL for manufacturing purposes<br>
<a href="https://cad.onshape.com/documents/71abd6fc3ce6fed7e6a05485/w/368905de720fe40a577fe632/e/d8a57b8590b4a5671c514ffa?renderMode=0&uiState=6729e07989212b582ec5eacb" target="_blank">View Design</a><br><br>

<strong>Quality Control and Feedback:</strong><br>
- Testing: Test clip functionality to ensure a satisfying "snap." If not achieved, client will provide design modifications.<br>
- Feedback: Client requires any assembly challenges or adjustments to be noted and reported.<br><br>

<strong>Production Timeline:</strong> Initial Prototype: As soon as humanly (or robotically) possible. Final Batch: Pending clip-test approval.<br><br>

<strong>Note:</strong> A highly professional order to add a sturdy flair to your cardboard-carrying adventures!
`,
                    status: true,
                    link: "https://cad.onshape.com/documents/71abd6fc3ce6fed7e6a05485/w/368905de720fe40a577fe632/e/d8a57b8590b4a5671c514ffa?renderMode=0&uiState=6729e07989212b582ec5eacb",
                    date: "2024-11-03"
                }
            ]


        };
    }
};
</script>