<template>
    <div class="main-component-div">
        <div class="star-icon-div">
            <img src="../images/icon-star.svg" alt="the image of star">
        </div>
        <h2>How did we do?</h2>
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
            <div class="mark one" :class="{markChecked: markOneChecked}" @click="markOneClicked">1</div>
            <div class="mark two" :class="{markChecked: markTwoChecked}" @click="markTwoClicked">2</div>
            <div class="mark three" :class="{markChecked: markThreeChecked}" @click="markThreeClicked">3</div>
            <div class="mark four" :class="{markChecked: markFourChecked}" @click="markFourClicked">4</div>
            <div class="mark five" :class="{markChecked: markFiveChecked}" @click="markFiveClicked">5</div>
        </div>

        <div class="submit" @click="submitClicked">SUBMIT</div>

    </div>
</template>

<script>
export default {
    // name: 'mainComponent',
    methods: {
        submitClicked(){
            this.$emit("main-component-submitted");
        },
        markOneClicked(){
            this.$emit("mark-one-clicked");
            this.markOneChecked = true;
            this.markTwoChecked = false;
            this.markThreeChecked = false;
            this.markFourChecked = false;
            this.markFiveChecked = false;
        },
        markTwoClicked(){
            this.$emit("mark-two-clicked");
            this.markOneChecked = false;
            this.markTwoChecked = true;
            this.markThreeChecked = false;
            this.markFourChecked = false;
            this.markFiveChecked = false;
        },
        markThreeClicked(){
            this.$emit("mark-three-clicked");
            this.markOneChecked = false;
            this.markTwoChecked = false;
            this.markThreeChecked = true;
            this.markFourChecked = false;
            this.markFiveChecked = false;
        },
        markFourClicked(){
            this.$emit("mark-four-clicked");
            this.markOneChecked = false;
            this.markTwoChecked = false;
            this.markThreeChecked = false;
            this.markFourChecked = true;
            this.markFiveChecked = false;
        },
        markFiveClicked(){
            this.$emit("mark-five-clicked");
            this.markOneChecked = false;
            this.markTwoChecked = false;
            this.markThreeChecked = false;
            this.markFourChecked = false;
            this.markFiveChecked = true;
        }
    },
    data() {
        return{
            markOneChecked: false,
            markTwoChecked: false,
            markThreeChecked: false,
            markFourChecked: false,
            markFiveChecked: false,
        };
    }
}

</script>

<style scoped>
    .main-component-div{
        border-radius: 20px;
        padding: 25px;
        background-color: #1f2630;
        box-sizing: border-box;
        max-width: 390px;
        height: 360px;
        margin: auto;
    }

    .star-icon-div{
        /* border: solid; */
        border-radius: 30px;
        background-color: #262d37;
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
        margin-bottom: 10px;
    }

    p{
        text-align: left;
        font-family: Overpass;
        font-size: 15px;
        font-weight: 400;
        color: hsl(217, 12%, 63%);
        margin-top: 10px;
        margin-bottom: 20px;
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

    .mark {
        border-radius: 30px;
        padding: 2px 1px 0px 1px;
        width: 45px;
        height: 45px;
        display: flex;
        justify-content: center;
        align-items: center;
        background-color: rgba(38,47,56,255);
        color: hsl(217, 12%, 63%);
        font-weight: 700;
        line-height: 20px;

    }

    .mark:hover {
        color: hsl(0, 0%, 100%);
        background-color: #fb7614;
        cursor: pointer;
    }

    .markChecked{
        background-color: hsl(216, 12%, 54%);
        color: white;
    }
    

    .submit{
        margin-top: 20px;
        border-radius: 20px;
        color: hsl(0, 0%, 100%);
        background-color: #fb7614;
        display: flex;
        justify-content: center;
        align-items: center;
        padding-top: 10px ;
        padding-bottom: 7px ;
    }

    .submit:hover {
        color: #fb7614;
        background-color: hsl(0, 0%, 100%);
        cursor: pointer;
    }

</style>