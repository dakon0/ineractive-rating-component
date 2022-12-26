<template>
    <div class="main-component-div">
        <div class="star-icon-div">
            <img src="../images/icon-star.svg" alt="the image of star">
        </div>
        <h1>How did we do?</h1>
        <p>Please let us know how we did with your support request. All feedback is appreciated 
           to help us improve our offering!</p>
        <!-- <form>
            <div class="checkboxes">
                <div class="checkbox one">
                    <input type="checkbox" id="one">
                    <label for="one">1</label>
                </div>
                <div class="checkbox two">
                    <input type="checkbox" id="two">
                    <label for="two">2</label>
                </div>
                <div class="checkbox three">
                    <input type="checkbox" id="three">
                    <label for="three">3</label>
                </div>
                <div class="checkbox four">
                    <input type="checkbox" id="four">
                    <label for="four">4</label>
                </div>
                <div class="checkbox five">
                    <input type="checkbox" id="five">
                    <label for="five">5</label>
                </div>
            </div>
            <div class="submit">
                <input type="submit" value="SUBMIT">
            </div>
        </form> -->
        <div class="marks">
            <div class="mark one">1</div>
            <div class="mark two">2</div>
            <div class="mark three">3</div>
            <div class="mark four">4</div>
            <div class="mark five">5</div>
        </div>

        <div class="submit" @click="submitClicked">SUBMIT</div>


        
    </div>
</template>

<script>
export default {
    // name: 'mainComponent',
    methods: {
        submitClicked(){
            console.log("submitClicked() called");
            this.$emit("main-component-submitted");
        }
    }
}
</script>

<style scoped>
    .main-component-div{
        border-radius: 20px;
        padding: 20px;
        background-color: hsl(213, 19%, 18%);
    }

    .star-icon-div{
        /* border: solid; */
        border-radius: 30px;
        background-color: hsl(216, 12%, 54%);
        display: flex;
        justify-content: center;
        align-items: center;
        width: 50px;
        height: 50px;
    }

    h1 {
        text-align: left;
        font-family: Overpass;
        color: hsl(0, 0%, 100%);
    }

    p{
        text-align: left;
        font-family: Overpass;
        font-size: 15px;
        font-weight: 400;
        color: hsl(217, 12%, 63%);
    }

    /* .checkbox {
        border: solid black;
        border-radius: 35px;
        width: 50px;
        height: 50px;
        background-color: hsl(216, 12%, 54%);
    }

    .checkbox label{
        color: hsl(217, 12%, 63%);
    }

    .checkboxes{
        display: flex;
        justify-content: space-between;
    } */

    .marks {
        display: flex;
        justify-content: space-between;
    }

    .mark{
        border-radius: 30px;
        /* padding-bottom: -1px; */
        width: 45px;
        height: 45px;
        display: flex;
        justify-content: center;
        align-items: center;
        background-color: hsl(216, 12%, 54%);
        color: hsl(217, 12%, 63%);
        font-weight: 700;
    }

    .mark:hover {
        color: hsl(25, 97%, 53%);
        background-color: hsl(0, 0%, 100%);
        cursor: pointer;
    }
    

    .submit{
        margin-top: 20px;
        border-radius: 20px;
        color: hsl(0, 0%, 100%);
        background-color: hsl(25, 97%, 53%);
        display: flex;
        justify-content: center;
        align-items: center;
        padding-top: 10px ;
        padding-bottom: 7px ;
    }

    .submit:hover {
        color: hsl(25, 97%, 53%);
        background-color: hsl(0, 0%, 100%);
        cursor: pointer;
    }

</style>