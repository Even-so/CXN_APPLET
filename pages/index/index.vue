<template>
    <view class="container">
        <view class="banner">
            <image
                src="https://img-shop.qmimg.cn/s23107/2020/04/26/3eb7808bf105262604.jpg"
                mode=""
                class="bg"
            ></image>
            <view class="intro">
                <view class="greet">您好，{{ isLogin ? member.nickname : "游客" }}</view>
                <view class="note">一杯奶茶，一口软欧包，在奈雪遇见两种美好</view>
            </view>
        </view>
        <view class="content">
            <view class="entrance">
                <view class="item" @tap="takein">
                    <image src="/static/images/index/zq.png" class="icon"></image>
                    <view class="title">自助点餐</view>
                </view>
                <view class="item" @tap="takeout">
                    <image src="/static/images/index/wm.png" class="icon"></image>
                    <view class="title">会员中心</view>
                </view>
            </view>
            <!-- <view class="info">
        <view class="integral_section" @tap="integrals">
          <view class="top">
            <text class="title">我的积分</text>
            <text class="value">411</text>
          </view>
          <view class="bottom">
            进入积分商城兑换奈雪券及周边好礼
            <view class="iconfont iconarrow-right"></view>
          </view>
        </view>
        <view class="qrcode_section" @tap="memberCode">
          <image src="/static/images/index/qrcode.png"></image>
          <text>会员码</text>
        </view>
      </view>
      <view class="navigators">
        <view class="left">
          <view class="grid flex-column just-content-center">
            <view class="d-flex align-items-center">
              <image
                src="/static/images/index/csc.png"
                class="mark-img"
              ></image>
              <view class="font-size-sm text-color-base">奈雪的茶商城</view>
            </view>
            <view
              class="text-color-assist"
              style="margin-left: 40rpx; font-size: 20rpx"
              >优质茶礼盒，网红零食</view
            >
          </view>
          <view class="grid justify-content-end align-items-end">
            <image
              src="/static/images/index/yzclh.png"
              class="yzclh-img"
              mode="heightFix"
            ></image>
          </view>
        </view>
        <view class="right">
          <view class="tea-activity" @tap="invite">
            <image src="/static/images/index/mcsb.png" class="mark-img"></image>
            <view>买茶送包</view>
            <view class="right-img">
              <image
                src="/static/images/index/mcsb_bg.png"
                mode="widthFix"
              ></image>
            </view>
          </view>
          <view class="member-gifts" @tap="packages">
            <image src="/static/images/index/hyjb.png" class="mark-img"></image>
            <view>会员劵包</view>
            <view class="right-img">
              <image
                src="/static/images/index/hyjb_bg.png"
                mode="widthFix"
              ></image>
            </view>
          </view>
        </view>
      </view> -->
            <view class="member-news">
                <view class="header">
                    <view class="title">会员新鲜事</view>
                    <!-- <view class="iconfont iconRightbutton"></view> -->
                </view>
                <view class="list">
                    <view class="item">
                        <image
                            src="https://img-shop.qmimg.cn/s23107/2020/04/27/0039bf41c9ebd50a2c.jpg"
                        ></image>
                        <view class="title">"梅"你不行 | 霸气杨梅清爽回归</view>
                    </view>
                </view>
            </view>
            <view class="mendian">
                <view class="header">
                    <view class="title">城市门店</view>
                </view>
                <view class="list">
                    <view class="headerList">
                        <span>最近门店（本市共3家门店）</span>
                        <view>
                            <span>全部50家门店</span>
                            <i class="iconfont iconRightbutton"></i>
                        </view>
                    </view>
                    <view class="item">
                        <view class="title">陈鲜柠（南油店）</view>
                        <view class="item-info">
                            <view class="item-info-left">
                                <i class="iconfont iconshouhuodizhi"></i>
                                <span>2.5km</span>
                                <span>营业时间：09：00-23：00</span>
                            </view>
                            <view class="item-info-right">
                                <i class="iconfont icon-qiepiandaohang"></i>
                                <i class="iconfont icon-dianhua-xianxingyuankuang"></i>
                            </view>
                        </view>
                    </view>
                    <view class="item">
                        <view class="title">陈鲜柠（南油店）</view>
                        <view class="item-info">
                            <view class="item-info-left">
                                <i class="iconfont iconshouhuodizhi"></i>
                                <span>2.5km</span>
                                <span>营业时间：09：00-23：00</span>
                            </view>
                            <view class="item-info-right">
                                <i class="iconfont icon-qiepiandaohang"></i>
                                <i class="iconfont icon-dianhua-xianxingyuankuang"></i>
                            </view>
                        </view> </view
                    ><view class="item">
                        <view class="title">陈鲜柠（南油店）</view>
                        <view class="item-info">
                            <view class="item-info-left">
                                <i class="iconfont iconshouhuodizhi"></i>
                                <span>2.5km</span>
                                <span>营业时间：09：00-23：00</span>
                            </view>
                            <view class="item-info-right">
                                <i class="iconfont icon-qiepiandaohang"></i>
                                <i class="iconfont icon-dianhua-xianxingyuankuang"></i>
                            </view>
                        </view> </view
                    ><view class="item">
                        <view class="title">陈鲜柠（南油店）</view>
                        <view class="item-info">
                            <view class="item-info-left">
                                <i class="iconfont iconshouhuodizhi"></i>
                                <span>2.5km</span>
                                <span>营业时间：09：00-23：00</span>
                            </view>
                            <view class="item-info-right">
                                <i class="iconfont icon-qiepiandaohang"></i>
                                <i class="iconfont icon-dianhua-xianxingyuankuang"></i>
                            </view>
                        </view>
                    </view>
                </view>
            </view>
        </view>
    </view>
</template>

<script>
import { mapState, mapGetters } from "vuex";

export default {
    data() {
        return {};
    },
    computed: {
        ...mapState(["member"]),
        ...mapGetters(["isLogin"]),
    },
    methods: {
        takein() {
            this.$store.commit("SET_ORDER_TYPE", "takein");
            uni.switchTab({
                url: "/pages/menu/menu",
            });
        },
        takeout() {
            if (!this.isLogin) {
                uni.navigateTo({ url: "/pages/login/login" });
                return;
            }
            uni.navigateTo({
                url: "/pages/address/address?is_choose=true",
            });
        },
        integrals() {
            if (!this.isLogin) {
                uni.navigateTo({ url: "/pages/login/login" });
                return;
            }
            uni.navigateTo({
                url: "/pages/integrals/integrals",
            });
        },
        packages() {
            uni.navigateTo({
                url: "/pages/packages/index",
            });
        },
        memberCode() {
            if (!this.isLogin) {
                uni.navigateTo({ url: "/pages/login/login" });
                return;
            }
            uni.navigateTo({
                url: "/pages/mine/member-code",
            });
        },
        invite() {
            uni.navigateTo({
                url: "/pages/activities/invite",
            });
        },
    },
};
</script>

<style lang="scss" scoped>
/* #ifdef H5 */
page {
    height: auto;
    min-height: 100%;
}
/* #endif */

.banner {
    position: relative;
    width: 100%;
    height: 600rpx;

    .bg {
        width: 100%;
        height: 600rpx;
    }

    .intro {
        position: absolute;
        top: calc(50rpx + var(--status-bar-height));
        left: 40rpx;
        color: #ffffff;
        display: flex;
        flex-direction: column;

        .greet {
            font-size: $font-size-lg;
            margin-bottom: 10rpx;
        }

        .note {
            font-size: $font-size-sm;
        }
    }
}

.content {
    padding: 0 30rpx;
}

.entrance {
    position: relative;
    margin-top: -80rpx;
    margin-bottom: 30rpx;
    border-radius: 10rpx;
    background-color: #ffffff;
    box-shadow: $box-shadow;
    padding: 30rpx 0;
    display: flex;
    align-items: center;
    justify-content: center;

    .item {
        flex: 1;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        position: relative;

        &:nth-child(1):after {
            content: "";
            position: absolute;
            width: 1rpx;
            background-color: #ddd;
            right: 0;
            height: 100%;
            transform: scaleX(0.5) scaleY(0.8);
        }

        .icon {
            width: 84rpx;
            height: 84rpx;
            margin: 20rpx;
        }

        .title {
            font-size: 30rpx;
            color: $text-color-base;
            font-weight: 600;
        }
    }
}

.info {
    position: relative;
    margin-bottom: 30rpx;
    border-radius: 10rpx;
    background-color: #ffffff;
    box-shadow: $box-shadow;
    padding: 30rpx;
    display: flex;
    align-items: center;
    justify-content: center;

    .integral_section {
        flex: 1;
        display: flex;
        flex-direction: column;
        justify-content: center;

        .top {
            display: flex;
            align-items: center;

            .title {
                color: $text-color-base;
                font-size: $font-size-base;
                margin-right: 10rpx;
            }
            .value {
                font-size: 44rpx;
                font-weight: bold;
            }
        }

        .bottom {
            font-size: $font-size-sm;
            color: $text-color-assist;
            display: flex;
            align-items: center;
        }
    }

    .qrcode_section {
        color: $color-primary;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        font-size: $font-size-sm;

        image {
            width: 40rpx;
            height: 40rpx;
            margin-bottom: 10rpx;
        }
    }
}

.navigators {
    width: 100%;
    margin-bottom: 20rpx;
    border-radius: 10rpx;
    background-color: #ffffff;
    box-shadow: $box-shadow;
    padding: 20rpx;
    display: flex;
    align-items: stretch;

    .left {
        width: 340rpx;
        margin-right: 20rpx;
        display: flex;
        padding: 0 20rpx;
        flex-direction: column;
        font-size: $font-size-sm;
        color: $text-color-base;
        background-color: #f2f2e6;

        .grid {
            height: 50%;
            display: flex;
        }
    }

    .right {
        width: 290rpx;
        display: flex;
        flex-direction: column;

        .tea-activity,
        .member-gifts {
            width: 100%;
            display: flex;
            padding: 20rpx;
            font-size: $font-size-sm;
            color: $text-color-base;
            align-items: center;
            position: relative;
        }

        .tea-activity {
            background-color: #fdf3f2;
            margin-bottom: 20rpx;
        }

        .member-gifts {
            background-color: #fcf6d4;
        }

        .right-img {
            flex: 1;
            position: relative;
            margin-left: 20rpx;
            margin-right: -20rpx;
            margin-bottom: -20rpx;
            display: flex;
            align-items: flex-end;

            image {
                width: 100%;
            }
        }
    }

    .mark-img {
        width: 30rpx;
        height: 30rpx;
        margin-right: 10rpx;
    }

    .yzclh-img {
        height: 122.96rpx;
        width: 214.86rpx;
    }
}

.member-news {
    width: 100%;
    margin-bottom: 30rpx;
    .header {
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding: 20rpx 0;

        .title {
            font-size: $font-size-lg;
            font-weight: bold;
        }

        .iconfont {
            font-size: 52rpx;
            color: $text-color-assist;
        }
    }

    .list {
        width: 100%;
        display: flex;
        flex-direction: column;

        .item {
            width: 100%;
            height: 240rpx;
            position: relative;

            image {
                width: 100%;
                height: 100%;
                border-radius: 8rpx;
            }

            .title {
                position: relative;
                font-size: 32rpx;
                font-weight: 500;
                width: 100%;
                top: -70rpx;
                left: 16rpx;
                color: #ffffff;
            }
        }
    }
}
.mendian {
    width: 100%;
    margin-bottom: 30rpx;
    .header {
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding: 20rpx 0;
        .title {
            font-size: $font-size-lg;
            font-weight: bold;
        }

        .iconfont {
            font-size: 52rpx;
            color: $text-color-assist;
        }
    }
    .list {
        background-color: $text-color-white;
        padding: 30rpx 20rpx;
        border-radius: 20rpx;
        .headerList {
            width: 100%;
            display: flex;
            align-items: center;
            justify-content: space-between;
            span {
                font-size: $font-size-sm;
                color: $text-color-assist;
            }
            .iconfont {
                margin-left: 10rpx;
                font-size: 24rpx;
                color: $text-color-assist;
                display: inline-block;
                vertical-align: middle;
            }
        }
        .item {
            padding-bottom: 10rpx;
            .title {
                font-size: $font-size-lg;
                font-weight: bold;
                margin: 20rpx 0 0rpx 0;
            }
            .item-info {
                display: flex;
                align-items: center;
                justify-content: space-between;
                .item-info-left {
                    display: flex;
                    align-items: center;
                    justify-content: space-between;
                    span {
                        font-size: $font-size-sm;
                        color: $text-color-grey;
                        margin-left: 20rpx;
                    }
                    .iconfont {
                        font-size: $font-size-sm;
                        color: $text-color-grey;
                    }
                }
                .item-info-right {
                    display: flex;
                    align-items: center;
                    justify-content: space-between;
                    .iconfont {
                        margin: 0 10rpx;
                        font-size: $img-size-sm;
                        color: $text-color-grey;
                    }
                }
            }
        }
    }
}
</style>
