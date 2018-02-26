<template>
    <div id="topbar">
        <div class="editingArea">
            <div class="logo">
                <svg class="icon">
                    <use xlink:href="#icon-wu"></use>
                </svg>
            </div>
            <el-menu :default-active="activeIndex" class="el-menu-demo" 
                    mode="horizontal" @select="handleSelect" active-text-color="#409EFF">
                <el-menu-item index="1">可视化编辑器</el-menu-item>
            </el-menu>
        </div>
        <div class="operationArea">
            <div class="action">
                <el-button plain>注册</el-button>
                <el-button plain>登录</el-button>
                <el-button plain>保存</el-button>
                <el-button plain>预览</el-button>
            </div>
            <div class="setup">
                <svg class="icon">
                    <use xlink:href="#icon-setup"></use>
                </svg>
            </div>
        </div>

    </div>
</template>



<script>
export default {
    data() {
      return {
        activeIndex: '1',
        activeIndex2: '1'
      };
    },
    methods: {
      handleSelect(key, keyPath) {
        console.log(key, keyPath);
      }
    }
  }

</script>

<style lang="scss">
    @import '../assets/mixin.scss';
    #topbar{
        @include flex(space-between, center);
        @mixin logoAndSetup($fill){
            @include widthHeight(60px, 60px);
            @include flex(center, center);
            >.icon{
                @include widthHeight(30px, 30px);
                fill: $fill;
            }
        }
        >div.editingArea{
            @include flex(flex-start, center);
            >div.logo{
                @include logoAndSetup(#4094E4);
                border-right: 1px solid #EEEEEE;
            }
            >.el-menu--horizontal{
                border: none;
                >.el-menu-item{
                    @include fontColor(14px, #999);
                    padding-left: 15px;
                    padding-right: 15px;
                    border-right: 1px solid #EEEEEE;
                    &.is-active{
                        border-bottom-width: 5px;
                    }
                }
             }
        }
        >div.operationArea{
            @include flex(flex-start, center);
            >div.action{
                padding-left: 15px;
                padding-right: 15px;
                >.el-button{
                    @include fontColor(16px, #3E94E4);
                    line-height: 25px;
                    border-color: #3E94E4;
                    padding: 8px 30px;
                    &:hover{
                        color: #fff;
                        background-color: #3E94E4;
                    }
                }
            }
            >div.setup{
                @include logoAndSetup(#888888);
                border-left: 1px solid #EEEEEE;
            }

        }
    }
</style>
