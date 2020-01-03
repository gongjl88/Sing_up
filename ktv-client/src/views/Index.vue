<template>
    <div class="index-view">
        <!-- 首页内容 -->
        <div class="content">
            <div class="left-content">
                <div class="top1">
                    <div class="left1">
                        <div style="width: 400px;" @click="goArtist"></div>
                    </div>
                    <div class="right1">
                        <div class="top2">  
                            <div class="left2"><div @click="goABC"></div></div>
                            <div class="right2"><div @click="goLanguage"></div></div>
                            
                        </div>
                        <div class="bottom2"><div @click="goStyle"></div></div>
                        
                    </div>
                </div>
                <div class="bottom1"><div @click="goKtvLikes"></div></div>
                <div class="right-collection" @click="goHot()"></div>
               
            </div>
            
            <div class="right-content" @click="goHot()"><div></div></div>
            
        </div>
        <div class="right-project" @click="goHot()"></div>
        <div class="right-classification" @click="goHot()"></div>
        
    </div>
</template>
<script>
import hasLogin from "@/config/isLogin";
export default {
    name:"index-view",
    data(){
        return{

        }
    },
    methods:{
        goHot(){
            if(hasLogin()){
                this.$router.push('/home/hot');
            }
        },
        goArtist(){
            if(hasLogin()){
                this.$router.push('/home/artist');
            }
        },
        goABC(){
            if(hasLogin()){
                this.$router.push('/home/abc');
            }
        },
        goLanguage(){
            if(hasLogin()){
                this.$router.push('/home/language');
            }
        },
        goStyle(){
            if(hasLogin()){
                this.$router.push('/home/style');
            }
        },
        goKtvLikes(){
            if(hasLogin()){
                this.$router.push('/home/ktvlikes');
            }
        }
    }
}
</script>
<style lang="less" scoped>
.index-view{
    width: 100%;
    height: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
    margin-left: 120px;
    overflow: hidden;
    .content{
        width: 1100px;
        height: 450px;
        
        display: flex;

        .left-content{
            width: 100%;
            flex: 3;
            display: flex;
            flex-direction: column;

            .top1{
                width: 100%;
                flex: 3;
                display: flex;

                .left1{
                    flex: 1;
                    height: 240px;
                    padding: 5px;
                    div{
                        // margin-bottom: 5px;
                        border-radius: 5px;
                        width: 100%;
                        height: 97%;
                        background-image: url(../assets/image/拼音点歌.gif);
                        background-repeat:no-repeat;
                        background-position: center;
                        transition: all 750ms;
                        &:hover{
                            transform: scale(1.03);
                            cursor: pointer;
                            box-shadow: 1px 1px 1px rgba(0, 0, 0, .4);
                        }
                    }
                    
                }
                .right1{
                    flex: 2;
                    height: 100%;
                    display: flex;
                    flex-direction: column;

                    .top2{
                        flex: 2;
                        width: 100%;
                        display: flex;
                        .left2{
                            flex: 1;
                            height: 100%;
                            padding: 5px;
                            div{
                                border-radius: 5px;
                                width: 250px;
                                height: 125%;
                                background-image: url(../assets/image/歌星.gif);
                                background-position: center; 
                                background-size: 100% 100%;
                                transition: all 750ms;
                                &:hover{
                                    transform: scale(1.03);
                                    cursor: pointer;
                                    box-shadow: 1px 1px 1px rgba(0, 0, 0, .4);
                                }
                            }
                        }
                        .right2{
                            flex: 1;
                            height: 100%;
                            padding: 5px;
                            div{
                                border-radius: 5px;
                                width: 209px;
                                height: 220px;
                                background-image: url(../assets/image/新歌.jpg);
                                background-position: center top; 
                                transition: all 750ms;
                                &:hover{
                                    transform: scale(1.03);
                                    cursor: pointer;
                                    box-shadow: 1px 1px 1px rgba(0, 0, 0, .4);
                                }
                            }
                        }
                    }
                    .bottom2{
                        flex: 1;
                        width: 100%;
                        height: 100%;
                        padding-top: 10px;
                        
                        div{
                            border-radius: 5px;
                             margin: -15px;
                            width: 200px;
                            height: 214px;
                            background-image: url(../assets/image/语言.gif);
                            margin-left:-405px;
                            /* background-size: 100% 120%; */
                            background-position: center;
                            transition: all 750ms;
                            &:hover{
                                transform: scale(1.03);
                                cursor: pointer;
                                box-shadow: 1px 1px 1px rgba(0, 0, 0, .4);
                            }
                        }
                    }
                }
            }
            .bottom1{
                width: 100%;
                flex:1;
                padding: 5px;
                div{
                    margin-right: 5px;
                    border-radius: 5px;
                    width: 200px;
                    height: 214px;
                    background-image: url(../assets/image/高清.gif);
                    margin-left:205px;
                    margin-top:-205px;
                    /* background-size: 100% 170%; */
                    background-position: center;
                    transition: all 750ms;
                    &:hover{
                        transform: scale(1.03);
                        cursor: pointer;
                        box-shadow: 1px 1px 1px rgba(0, 0, 0, .4);
                    }
                }
            }
        }
        .right-content{
            width: 100%;
            flex: 1;
            padding: 5px;
            div{
                border-radius: 5px;
                width: 207px;
                height: 219px;
                background-image: url(../assets/image/排行.gif);
                background-position: center top;
                transition: all 750ms;
                &:hover{
                    transform: scale(1.03);
                    cursor: pointer;
                    box-shadow: 1px 1px 1px rgba(0, 0, 0, .4);
                }
            }
        }
        
    }
}
.right-collection{
    width: 244px;
    height: 151px;
    background-image: url(../assets/image/收藏.gif);
    background-repeat:no-repeat;
    margin-left: 422px;
    margin-top: -290px;
    flex: 1;
    padding: 5px;
    transition: all 750ms;
}
.right-collection:hover{
                    transform: scale(1.03);
                    cursor: pointer;
                    box-shadow: 1px 1px 1px rgba(0, 0, 0, .4);
                }
.right-project{
    width: 210px;
    height: 213px;
    background-image: url(../assets/image/专题.gif);
    background-repeat:no-repeat;
    
    margin-top: 240px;
    margin-left: -420px;
    
    
    transition: all 750ms;
}
.right-project:hover{
    transform: scale(1.03);
                    cursor: pointer;
                    /* box-shadow: 1px 1px 1px rgba(0, 0, 0, .4); */
}

.right-classification{
    width: 210px;
    height: 213px;
    background-image: url(../assets/image/分类.gif);
    background-repeat:no-repeat;
    
    margin-top: 240px;
    margin-left: 10px;
    flex: 1;
    
    transition: all 750ms;
}
.right-classification:hover{
    transform: scale(1.03);
                    cursor: pointer;
                    /* box-shadow: 1px 1px 1px rgba(0, 0, 0, .4); */
}
</style>