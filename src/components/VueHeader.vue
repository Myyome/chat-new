<template>
    <div class="xw-header">
         <div class="xw-header-content" >
	              <div>
	                <img src="../assets/logo.jpg" class="xw-header-avatar">
	                <div class="xw-header-title-wrap">
	                  <div class="xw-header-title">小群客服</div>
	                </div>
	              </div>
	        </div>
    </div>
</template>
<script>
export default {
  
}
</script>
<style>
.xw-header {
  z-index: 2;
  max-height: 3.6rem;
  background: #5a7fb0;
  box-shadow: 0 1px 3px rgba(0, 0, 0, .2);
}

.xw-header-content {
  position: relative;
  overflow: hidden;
  padding: 0px 0.16rem;
  min-height: 0.5rem;
}
.xw-header-avatar {
  float: left;
  height: 0.4rem;
  width: 0.4rem;
  border-radius: 100%;
  box-shadow: 0 2px 4px rgba(0, 0, 0, .1);
  margin-right: 0.08rem;
  margin-top: -0.03rem;
}
.xw-header-title {
  font-size: 0.14rem;
  color: #fff;
  margin-top: 0.08rem;
}
</style>