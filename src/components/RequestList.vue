<template>
    <div>
        <RequestItem v-for="request in [...requests].sort((a, b) => new Date(b.date) - new Date(a.date))"
            :key="request.id" :request="request" />
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
                },
                {
                    id: 3,
                    name: "Bathroom Floor Heating Automation Module",
                    description: "A 2-part module designed to automate the heating system for bathroom floors.",
                    shortDescription: "2-part module to automate bathroom floor heating.",
                    longDescription: `
<strong>3D Printing Factory Order Slip</strong><br>
<strong>Client:</strong> Nejc Kovačič<br>
<strong>Order ID:</strong> BFH-2024-004<br><br>

<strong>Item Details:</strong><br>
<strong>Product Name:</strong> Bathroom Floor Heating Automation Module<br>
<strong>Parts:</strong> 2 (1 Base, 1 Cover)<br>
<strong>Material:</strong> PLA (preferred white or closest available shade)<br>
<strong>Color:</strong> Preferably white<br>
<strong>Function:</strong> A structural module to enclose and automate the heating system for bathroom floors, ensuring secure and efficient housing for components.<br><br>

<strong>Production Specifications:</strong><br>
- Quantity: 1 set (1 Base, 1 Cover)<br>
- Design Considerations: Ensure the parts fit together securely with tight tolerances to maintain structural integrity.<br>
- Assembly Test: Verify the parts interlock and provide sufficient space for internal components. Feedback on dimensions and assembly ease is appreciated.<br>
- Design Export: Accessible via the following link for manufacturing:<br>
<a href="https://cad.onshape.com/documents/fec1792d1ba7c8375931ca82/w/9c8474954c368ab498207504/e/06f893a5d03aa683a2329f9e?renderMode=0&uiState=6750fefba5c0872f8c06c771" target="_blank">View Design</a><br><br>

<strong>Quality Control and Feedback:</strong><br>
- Fit and Function: Ensure that the module’s parts align properly and can accommodate any internal components.<br>
- Feedback Needed: Provide notes on dimensional accuracy and any adjustments needed for assembly.<br><br>

<strong>Production Timeline:</strong> Prototype Requested: As soon as possible, followed by feedback for adjustments if needed.<br><br>

<strong>Note:</strong> Designed for practical automation with emphasis on fit and functionality over aesthetics.
`,
                    status: true,
                    link: "https://cad.onshape.com/documents/fec1792d1ba7c8375931ca82/w/9c8474954c368ab498207504/e/06f893a5d03aa683a2329f9e?renderMode=0&uiState=6750fefba5c0872f8c06c771",
                    date: "2024-12-06"
                },
                {
                    id: 4,
                    name: "Bathroom Floor Heating Automation Module (Lever Reprint)",
                    description: "Reprinting the lever for the bathroom floor heating automation module due to incorrect dimensions.",
                    shortDescription: "Reprint of the lever for bathroom floor heating module.",
                    longDescription: `
<strong>3D Printing Factory Order Slip</strong><br>
<strong>Client:</strong> Nejc Kovačič<br>
<strong>Order ID:</strong> BFH-2024-005<br><br>

<strong>Item Details:</strong><br>
<strong>Product Name:</strong> Bathroom Floor Heating Automation Module (Lever Reprint)<br>
<strong>Parts:</strong> 1 (Lever only)<br>
<strong>Material:</strong> PLA <br>
<strong>Color:</strong> Preferably Pink<br>
<strong>Function:</strong> Reprinting the lever to correct dimensional inaccuracies. This part is critical to the module's function and requires precise tolerances.<br><br>

<strong>Production Specifications:</strong><br>
- Quantity: 1 (Lever only)<br>
- Design Considerations: Focus on dimensional accuracy to ensure proper fit with other module parts.<br>
- Design Export: Accessible via the following link for manufacturing:<br>
<a href="https://cad.onshape.com/documents/fec1792d1ba7c8375931ca82/w/9c8474954c368ab498207504/e/06f893a5d03aa683a2329f9e?renderMode=0&uiState=6750fefba5c0872f8c06c771" target="_blank">View Design</a><br><br>
`,
                    status: true,
                    link: "https://cad.onshape.com/documents/fec1792d1ba7c8375931ca82/w/9c8474954c368ab498207504/e/06f893a5d03aa683a2329f9e?renderMode=0&uiState=6750fefba5c0872f8c06c771",
                    date: "2024-12-08"
                },
                {
                    id: 5,
                    name: "Bathroom Floor Heating Automation Module (Updated Lever - AGAIN)",
                    description: "Reprint of the lever for the bathroom floor heating automation module after design modifications to correct issues with the previous print.",
                    shortDescription: "Reprint of the updated lever for bathroom floor heating automation module.",
                    longDescription: `
<strong>3D Printing Factory Order Slip</strong><br>
<strong>Client:</strong> Nejc Kovačič<br>
<strong>Order ID:</strong> BFH-2024-006<br><br>

<strong>Item Details:</strong><br>
<strong>Product Name:</strong> Bathroom Floor Heating Automation Module<br>
<strong>Parts:</strong> 1 (Updated Lever)<br>
<strong>Material:</strong> PLA (preferred white or closest available shade)<br>
<strong>Color:</strong> Preferably white<br>
<strong>Function:</strong> Reprinting the updated lever component for the module. The design has been modified to address dimensional inaccuracies observed in the previous print.<br><br>

<strong>Production Specifications:</strong><br>
- Quantity: 1 (Updated Lever)<br>
- Design Focus: Ensure the updated dimensions allow proper integration with the existing module components (base and cover).<br>
- Design Export: Accessible via the following link for manufacturing:<br>
<a href="https://cad.onshape.com/documents/fec1792d1ba7c8375931ca82/w/9c8474954c368ab498207504/e/06f893a5d03aa683a2329f9e?renderMode=0&uiState=6750fefba5c0872f8c06c771" target="_blank">View Updated Design</a><br><br>
<strong>Note:</strong> This order focuses on the updated lever design. Dimensional accuracy and functional fit remain the priorities for testing.
`,
                    status: false,
                    link: "https://cad.onshape.com/documents/fec1792d1ba7c8375931ca82/w/9c8474954c368ab498207504/e/06f893a5d03aa683a2329f9e?renderMode=0&uiState=6750fefba5c0872f8c06c771",
                    date: "2024-12-09"
                },
                {
                    id: 6,
                    name: "Under the Desk Control Panel v2",
                    description: "A 7-part control panel designed to fit under a desk, featuring square and circular buttons and a sleek casing.",
                    shortDescription: "Under-desk control panel with buttons and casing.",
                    longDescription: `
<strong>3D Printing Factory Order Slip</strong><br>
<strong>Client:</strong> Nejc Kovačič<br>
<strong>Order ID:</strong> UDC-2024-007<br><br>

<strong>Item Details:</strong><br>
<strong>Product Name:</strong> Under the Desk Control Panel v2<br>
<strong>Parts:</strong> 7 (4 square buttons, 1 circular button, 1 casing, 1 front panel)<br>
<strong>Material:</strong> Any color will do—bonus points if it stands out 🌈<br>
<strong>Function:</strong> A fun yet functional control panel to mount under a desk.<br><br>

<strong>Production Specifications:</strong><br>
- Quantity: 1 full set (7 parts)<br>
- Tolerances: Designed with small tolerances. Please test and confirm if assembly works smoothly.<br>
- Design Export: Access the design here:<br>
<a href="https://cad.onshape.com/documents/75039cd5821e3dfc6467f0d0/w/14d6594fbebf820875ff4dd8/e/39d327768d0d7a1ae0b2a855?renderMode=0&uiState=675aba958e537b0ed9ca3817" target="_blank">View Design</a><br><br>

<strong>Quality Control and Feedback:</strong><br>
- Fit Test: Verify buttons fit the casing properly without resorting to creative force.<br>
- Feedback Needed: Let me know if the tolerances are too tight or if things need adjustments.<br><br>

<strong>Production Timeline:</strong> Whenever you’re ready to make under-desk magic happen!<br><br>

<strong>Note:</strong> It’s a control panel—practical, but it wouldn’t hurt if it looked fabulous!
`,
                    status: false,
                    link: "https://cad.onshape.com/documents/75039cd5821e3dfc6467f0d0/w/14d6594fbebf820875ff4dd8/e/39d327768d0d7a1ae0b2a855?renderMode=0&uiState=675aba958e537b0ed9ca3817",
                    date: "2024-12-12"
                },
                {
                    id: 7,
                    name: "Toothbrush Cup Cover",
                    description: "A simple cover to transform a regular cup into a toothbrush holder.",
                    shortDescription: "Cup cover to turn it into a toothbrush holder.",
                    longDescription: `
<strong>3D Printing Factory Order Slip</strong><br>
<strong>Client:</strong> Nejc Kovačič<br>
<strong>Order ID:</strong> TCC-2024-008<br><br>

<strong>Item Details:</strong><br>
<strong>Product Name:</strong> Toothbrush Cup Cover<br>
<strong>Parts:</strong> 1 (Cup Cover)<br>
<strong>Material:</strong> Any available color (please let me know the options so I can check with my mom 🌈)<br>
<strong>Function:</strong> A cover designed to fit over a cup, converting it into a toothbrush holder.<br><br>

<strong>Production Specifications:</strong><br>
- **Quantity:** 1<br>
- **Design Export:** Access the design here:<br>
<a href="https://cad.onshape.com/documents/6a3db667a9c813f95b53c510/w/22f6a31166dd13a13a8a418d/e/b357a85dd7fdbbf0c763834a" target="_blank">View Design</a><br><br>

<strong>Production Timeline:</strong> No rush—whenever you have time!<br><br>

<strong>Note:</strong> Please let me know the color options so I can check with my mom before printing.
`,
                    status: false,
                    link: "https://cad.onshape.com/documents/6a3db667a9c813f95b53c510/w/22f6a31166dd13a13a8a418d/e/b357a85dd7fdbbf0c763834a",
                    date: "2024-12-14"
                }



            ]
        };
    }
};
</script>