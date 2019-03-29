<template>
     <div class="xw-footer-wrap">
          <div class="xw-footer-content">
            <div class="xw-vmodel-wrap">
               <textarea class="xw-content-textarea" placeholder="请输入您的问题" ></textarea>
            </div>
            <!-- <div class="xw-chat-tool">
              <div class="xw-chat-tool-item">
                  <transition  name="fade">
                      <a href="javascript:void(0)" class="xw-send-btn-text" >发送</a>
                  </transition >
              </div>
            </div> -->
          </div>
        </div>
</template>
<style>
 .xw-footer-wrap {
    justify-content:flex-end;
    width: 100%;
    box-shadow: 0 -1px 4px rgba(0, 0, 0, .05);
    background: #fff;
    z-index: 2;
    position: absolute;
    bottom: 0;
}

.xw-footer-content {
  position: relative;
  height: 52px;
  display: flex;
 box-shadow: rgba(0, 0, 0, 0.05) 0px -1px 4px;
}
.xw-vmodel-wrap{
  flex:1;
}
.xw-content-textarea{
  box-sizing: border-box;
  z-index: 1;
  overflow-y: auto;
  font-size: 14px;
  line-height: 14px;
  border: none;
  resize: none;
  padding: 16px 85px 16px 14px;
  font-family: inherit;
  white-space: pre;
  white-space: pre-wrap;
  word-wrap: break-word;
}
</style>