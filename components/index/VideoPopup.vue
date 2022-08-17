<template>
  <div id="cover_layer">
    <div id="video-card">
        <div id="top-bar">
            <button id="close-btn" @click="closeVideo()">✖</button>
        </div>
        <div id="video-ctn">

        </div>
    </div>
  </div>
</template>

<script>
export default {
    props: ['closeVideo']

}
</script>


<style lang="scss" scoped>
    #cover_layer {
        position: fixed;
        top: 0;
        width: 100vw;
        height: 100vh;
        z-index: 999;
        display: flex;
        justify-content: center;
        align-items: center;
        background: rgb(255, 255, 255, 80%);
        #video-card {
            display: flex;
            flex-flow: column nowrap;
            background: white;
            border-radius: 8px;
            box-shadow: 0 0 20px gray;
            box-sizing: border-box;
            width: 800px;
            height: 600px;
            #top-bar {
                align-self: flex-start;
                display: flex;
                flex-flow: row nowrap;
                width: 100%;
                padding: 10px 25px 10px 0;
                #close-btn {
                    margin-left: auto;
                    background: none;
                    color: black;
                    font-size: 25px;
                }
            }
            #video-ctn {
                width: 100%;
                height: 100%;
                border-radius: 8px;
            }
        }
    }
</style>