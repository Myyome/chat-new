<template>
    <div class="xw-content"   ref="xwBody">    
        <div class="xw-chat-wrap" >
            <ul>
              <li v-for="record in records">
                <div v-if="record.type==1">
                  <div class="xw-chat-time">{{record.time}}</div>
                  <div class="xw-chat-servicer">
                    <div class="xw-servicer-avantar-wrap">
                      <img
                        src="../assets/logo.jpg" class="xw-servicer-avantar">
                    </div>
                    <div class="xw-chat-msg">
                      <span>{{record.content}}</span>
                    </div>
                  </div>
                </div>
                 <!-- 用户发送的消息模板-->
                <div v-else>
                  <div class="xw-chat-time">{{record.time}}</div>
                  <div class="xw-chat-customer">
                    <div class="xw-customer-avantar-wrap">
                      <img src="../assets/headImage.jpg" class="xw-customer-avantar">
                    </div>
                    <div class="xw-chat-msg" style="display:inline-block">
                      <span>{{record.content}}</span>
                    </div>
                  </div>
                </div>
              </li>
            </ul>
        </div>
		</div>
</template>
<script>
export default {
    data() {
        return {
            records:[
                {
                    type:1,
                    time:new Date().toLocaleTimeString(),
                    content:'您好！欢迎来到小群客服，请问有什么能帮到您？感谢您的支持!'
                }
                ,
                 {
                    type:2,
                    time:new Date().toLocaleTimeString(),
                    content:'谢谢您的帮助'
                }
            ]
        }
    }
}
</script>

<style>
.xw-chat-servicer:after,
.xw-chat-servicer:before,
.xw-chat-customer:after,
.xw-chat-customer:before,
.xw-chat-wrap:after,
.xw-chat-wrap:before,
.xw-chat-tool:after,
.xw-chat-tool:before,
.xw-chat-ul-box:after,
.xw-chat-ul-box:before {
  display: table;
  content: "";
  clear: both;
}

.xw-chat-wrap {
  overflow: auto;
  padding-left: 0.16rem;
  padding-bottom: 0.2rem;
}

.xw-chat-wrap .xw-chat-time,
.xw-chat-wrap time {
  line-height: 1;
  text-align: center;
  display: block;
  margin-bottom: 0.08rem;
  margin-top: 0.08rem;
  font-size: 0.12rem;
  color: #999;
  text-shadow: 1px 1px 1px hsla(0, 0%, 100%, .6);
}

.xw-chat-servicer,
.xw-chat-customer {
  position: relative;
  margin-bottom: 0.16rem;
  padding: 0 0.1rem 0 0.45rem;
}

.xw-servicer-avantar-wrap {
  position: absolute;
  bottom: 0;
  line-height: 0;
}
.xw-send-btn-text{
  padding: 0.04rem 0.08rem;
  background-color:#5a7fb0;
  color: #fff;
  border-radius: 0.05rem;
}
.xw-customer-avantar-wrap {
  position: absolute;
  bottom: 0;
  right: 8px;
  line-height: 0;
}

.xw-chat-servicer .xw-servicer-avantar-wrap,.xw-customer-avantar-wrap{
  left: 0;
}

.xw-servicer-avantar {
  border-radius: 100%;
}

.xw-servicer-avantar-wrap img,.xw-customer-avantar-wrap img {
  height: 0.34rem;
  width: 0.34rem;
}

.xw-chat-msg {
  -webkit-font-smoothing: antialiased;
  hyphens: auto;
  word-wrap: break-word;
  word-break: normal;
  position: relative;
  clear: both;
  padding: 0.08rem 0.16rem;
  border: 1px solid transparent;
  max-width: 100%;
  min-width: 0.5rem;
  min-height: 0.22rem;
  line-height: 0.16rem;
  max-width: 70%;
  font-size: 0.12rem;

}

.xw-chat-servicer .xw-chat-msg {
  background: #fff;
  border-color: #efefef;
  float: left;
}

.xw-chat-msg :last-child {
  margin-bottom: 0;
}

.xw-chat-msg span{
  white-space: pre-line;
}
.xw-chat-servicer,
.xw-chat-customer {
  position: relative;
  margin-bottom: 16px;
  padding: 0 10px 0 45px;
}

.xw-chat-customer {
  text-align: right;
}

.xw-chat-customer .xw-chat-msg {
  float: right;
  text-align: left;
  background: #5a7fb0;
  border-color: #5a7fb0;
  color: #fff;
  margin-right: 45px;
}
.xw-customer-avantar{
  border-radius: 50%;
}
.xw-chat-msg :last-child {
  margin-bottom: 0;
}

.xw-chat-wrap .xw-system-info-time,
.xw-chat-wrap time {
  line-height: 1;
  text-align: center;
  display: block;
  margin-bottom: 8px;
  font-size: 12px;
  color: #999;
  text-shadow: 1px 1px 1px hsla(0, 0%, 100%, .6);
}

.xw-chat-servicer:after,
.xw-chat-customer:after,
.xw-chat-wrap:after,
.xw-chat-tool:after,
.xw-chat-ul-box:after{
  clear: both;
}

.xw-chat-msg:last-child:before {
  bottom: -1px;
}

.xw-chat-msg:last-child:after,
.xw-chat-msg:last-child:before {
  content: "";
  position: absolute;
  height: 0;
  width: 0;
  display: block;
}

.xw-chat-customer .xw-chat-msg:last-child:before {
  display: inline-block;
  height: 0;
  width: 0;
  border: 10px solid transparent;
  border-bottom: 10px solid #5a7fb0;
  right: -10px;
  border-left-width: 9px;
}

.xw-chat-servicer .xw-chat-msg:last-child:before {
  display: inline-block;
  height: 0;
  width: 0;
  border: 10px solid transparent;
  border-bottom: 0.1rem solid #efefef;
  left: -10px;
  border-left-width: 0.09rem;
}

.xw-chat-servicer .xw-chat-msg:last-child:after {
  display: inline-block;
  height: 0;
  width: 0;
  border: 0.1rem solid transparent;
  border-bottom: 0.1rem solid #fff;
  left: -0.08rem;
  border-left-width: 0.09rem;
  bottom: 0px;
}

</style>
