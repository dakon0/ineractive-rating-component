<template>
    <div class="thanks-component-div">
        <div class="thanks-image-div">
            <img src="../images/illustration-thank-you.svg" alt="am image saying 'thank you!'.">
        </div>
        <div class="selected-mark"><p>You selected {{ markNumber }} of 5</p></div>
        <h2>Thank you!</h2>
        <p>We appreciate you taking the time to give a rating. If you ever need more support, 
           don't hesitate to get in touch!</p>
    </div>
</template>

<script>
    export default {
        props: {
            markNumber: {
                type: Number,
                required: true
            }
        }
    }
</script>
    
<style>
    .thanks-component-div {
        border-radius: 20px;
        padding:40px 25px;

        background-color: #1d242e;
        box-sizing: border-box;
        max-width: 390px;
        height: 360px;
        margin: auto;
        text-align: center;
    }

    h2 {
        font-family: Overpass;
        color: hsl(0, 0%, 100%);
        margin-bottom: 15px;
    }

    p{
        font-family: Overpass;
        font-size: 15px;
        font-weight: 400;
        color: hsl(217, 12%, 63%);
        
    }

    .selected-mark {
        background-color: #232e37;
        border-radius: 15px;
        width: 160px;
        margin: 25px auto;
        display: flex;
        justify-content: center;
    }

    .selected-mark p {
        color: hsl(25, 97%, 53%);
        margin-top:6px;
        margin-bottom: 2px;
        
    }

</style>