<template>
  <div class="detail">
    <div class="videos_content">
      <div class="video_content">
        <div class="video_box">
          <iframe
            width="100%"
            height="100%"
            src="https://www.youtube.com/embed/Wsdx1P_T-WM"
          ></iframe>
          <div class="headers_content">
            <div class="video_left_side">
              <div class="video_views_box">
                <div class="video_views">
                  <img src="../assets/video/likes.svg" alt="" />
                  <div class="video_views_count">100 345</div>
                </div>
                <div class="video_views">
                  <img src="../assets/video/viewers.svg" alt="" />
                  <div class="video_views_count">100 345</div>
                </div>
              </div>

              <div class="video_name">
                Figma Tutorial: Setup a Responsive Grid Layout for UI & Web
                Design (IN 11 MINUTES)
              </div>
            </div>
            <div class="video_rigth_side">
              <img src="../assets/video/chanel_logo.svg" alt="" />
              <div class="channel_creater">
                <div class="channel_name">Helen_NFT</div>
                <div class="channel_subs">245, 511 members</div>
              </div>
            </div>
          </div>
          <!-- <div class="pause_content">
            <img
              class="pause_icon"
              src="../assets/video/pause-icon.svg"
              alt=""
            />
          </div> -->
          <div class="comment_content">
            <commentBox :name="'WOW ... well said man. Great video. 🔥🔥🔥'" :src="'src/assets/video/comments.svg'"/>
            <commentBox :name="'WOW ... 🔥🔥🔥'" :src="'src/assets/video/comments.svg'"/>
            <commentBox :name="'WOW ... 🔥🔥🔥'" :src="'src/assets/video/comments.svg'"/>
          </div>
          <!-- <div class="timeline_content">
            <img
              style="margin-right: 30px; margin-top: 11px"
              src="../assets/video/timeline/pause-on-video.svg"
              alt=""
            />
            <img
              style="margin-right: 25px"
              src="../assets/video/timeline/sound.svg"
              alt=""
            />
            <div class="time">5: 14</div>
            <div class="timeline">
              <div class="timeline active"></div>
            </div>
            <div class="time">10: 32</div>
            <img
              style="margin-right: 27px"
              src="../assets/video/timeline/video-icon.svg"
              alt=""
            />
            <img
              style="margin-right: 27px"
              src="../assets/video/timeline/medium-scrin.svg"
              alt=""
            />
            <img src="../assets/video/timeline/full-scrin.svg" alt="" />
          </div> -->
        </div>
        <div class="video_info_box">
          <div class="tags_box">
            <div class="tags_item">#ETH-NFT</div>
            <div class="tags_item">#NFT-Trading</div>
          </div>
          <div class="video_titles">
            <div class="video_main_name">
              Figma Tutorial: Setup a Responsive Grid Layout for UI & Web Design
              (IN 11 MINUTES)
            </div>
            <div class="video_views_box">
              <div class="video_views">
                <img src="../assets/video/likes.svg" alt="" />
                <div class="video_views_count">100 345</div>
              </div>
              <div class="video_views">
                <img src="../assets/video/viewers.svg" alt="" />
                <div class="video_views_count">100 345</div>
              </div>
            </div>
          </div>
          <div class="channel_info">
            <div class="channel_content">
              <img src="../assets/icons/chanel_logos.svg" alt="" />
              <div class="channel_main_info">
                <div class="channel_main_name">Bankless</div>
                <div class="channel_main_views">12.455 members</div>
              </div>
            </div>

            <div class="channel_subscribe">subscribe</div>
            <div class="channel_base_info">
              <div class="channel_value">113</div>
              <div class="channel_key">Total Volume</div>
            </div>
            <div class="channel_base_info">
              <div class="channel_value">113</div>
              <div class="channel_key">Total Volume</div>
            </div>
          </div>
          <div class="comments_content">
            <div class="comments">
              01 November, 2022<br />
              It’s time to break up with your bank, and join the movement for
              sovereign finance. <br />
              👉 Build your crypto know-how by subscribing to the #Bankless
              newsletter.<br />
            </div>
          </div>
        </div>
      </div>

      <div class="playlist_content" style="height: 90vh">
        <div class="lines_content">
          <div class="line_btn" :class="{'active': currentTab === 1}" @click="currentTab = 1">
            <img src="../assets/lines/videos-icon.svg" alt="" />
            <div class="line_title">Videos</div>
          </div>
          <div class="line_btn" :class="{'active': currentTab === 2}" @click="currentTab = 2">
            <img src="../assets/lines/commments-icon.svg" alt="" />
            <div class="line_title">Comments</div>
          </div>
          <div class="line_btn" :class="{'active': currentTab === 3}" @click="currentTab = 3">
            <img src="../assets/lines/clips-icon.svg" alt="" />
            <div class="line_title">Clips</div>
          </div>
        </div>
        <div class="recomends_video_wrap" v-if="currentTab === 1">
          <div class="recomends_video" v-for="item in 10" :key="item">
            <img src="../assets/icons/video1.svg" alt="" />
            <div class="recomends_video_info">
              <div class="recomend_title">
                Lorem Ipsum is simply dummy text of the printing and typesetting
                industry. Lorem
              </div>
              <div class="recomend_author">Jack Jackson</div>
              <div class="video_views_box">
                <div class="video_views">
                  <img src="../assets/video/likes.svg" alt="" />
                  <div class="video_views_count">100 345</div>
                </div>
                <div class="video_views">
                  <img src="../assets/video/viewers.svg" alt="" />
                  <div class="video_views_count">100 345</div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="comments comments_main" v-if="currentTab === 2">
          <comment :image="'src/assets/comment-1.png'" :name="'asd'" :text="'good'" :date="'1 day ago'"/>
          <comment :image="'src/assets/comment-1.png'" :name="'ssss'" :text="'goodasdtd'" :date="'1 day ago'"/>
          <comment :image="'src/assets/comment-1.png'" :name="'hth'" :text="'asdadqwe'" :date="'2 days ago'"/>
          <comment :image="'src/assets/comment-1.png'" :name="'asddgt'" :text="'dafert'" :date="'2 days ago'"/>
        </div>
      </div>
    </div>
  </div>
</template>
  
<script>
import Comment from "@/components/comments/comment.vue";
import CommentBox from "@/components/comments/commentBox.vue";

export default {
  name: "DetailVideo",
  components: {Comment, CommentBox},
  data() {
    return {
      currentTab: 1,
    };
  },
  methods: {
    
  },
};
</script>
  
  <style scoped lang="scss">
.detail {
  color: #ffffff;
  display: flex;
  flex-direction: column;
}
.videos_content {
  display: flex;
  align-items: flex-start;
  /* height: 80vh; */
  overflow-y: scroll;
}
/* Video Content */
.video_content {
  height: calc(100vh - 200px);
  overflow-y: scroll;
  width: 60%;
  position: relative;
  /* background: url("../assets/icons/video_bg.jpg") no-repeat; */
  opacity: 0.7;
}

/* 1 - Video Box */
.video_box {
  position: relative;
  display: flex;
  flex-direction: column;
  margin-bottom: 42px;
  aspect-ratio: 16/9;
  width: 100%;
}
.headers_content {
  position: absolute;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 60px 48px 0 40px;
}

/* Video left side */
.video_left_side {
  /* position: absolute; */
  display: flex;
  flex-direction: column;
}
.video_views_box {
  display: flex;
  align-items: center;
  margin-bottom: 14px;
  cursor: pointer;
}
.video_views {
  display: flex;
  align-items: center;

  img {
    aspect-ratio: auto !important;
  }
}
.video_views:not(:last-child) {
  margin-right: 31px;
}
.video_views_count {
  margin-left: 8px;
  font-weight: 400;
  font-size: 20px;
}

.video_name {
  max-width: 650px;
  font-weight: 400;
  font-size: 30px;
}

/* video rigth side */
.video_rigth_side {
  position: absolute;
  right: 30px;
  display: flex;
  align-items: center;
}
.channel_creater {
  margin-left: 17px;
}
.channel_name {
  font-weight: 400;
  font-size: 28px;
}
.channel_subs {
  font-weight: 400;
  font-size: 24px;
  color: #a9a9b7;
}

/* Pause */
.pause_content {
  position: absolute;
  top: 35%;
  left: 45%;
  z-index: 2;
  border-radius: 50%;
  width: 133px;
  height: 133px;
  background: rgba(0, 0, 0, 0.35);
  box-shadow: 0px 4px 44px rgba(0, 0, 0, 0.45);
  backdrop-filter: blur(42px);
}
.pause_icon {
  position: absolute;
  top: 31%;
  left: 38%;
}

/* Comment */
.comment_content {
  position: absolute;
  bottom: 40px;
  right: 20px;
  display: flex;
  flex-direction: column;
  margin-top: auto;
  margin-bottom: 20px;
}

/* Timeline */
.timeline_content {
  display: flex;
  align-items: center;
  width: 100%;
  height: 80px;
  opacity: 0.4;
  background: #000000;
  padding: 27px 50px;
}
.time {
  font-weight: 400;
  font-size: 21px;
  margin-right: 17px;
}
.timeline {
  width: 1095px;
  height: 6px;
  background: #2c2c35;
  border-radius: 4.5px;
  margin-right: 12px;
}
.timeline .active {
  width: 488px;
  background: linear-gradient(273.27deg, #00eaf2 0.47%, #ea00d5 99.64%);
  border-radius: 4.5px;
}

/* 2 - Video Info Box */
.video_info_box {
  padding-left: 51px;
}
/* Tags */
.tags_box {
  display: flex;
  align-items: center;
}
.tags_item {
  padding: 10px;
  color: #6bb8ff;
  background: #15131c;
  font-weight: 400;
  font-size: 19px;
  margin-right: 7px;
}
/* Video Title */
.video_titles {
  margin-bottom: 50px;
}
.video_main_name {
  font-weight: 400;
  font-size: 30px;
  margin-bottom: 13px;
}

.channel_info {
  display: flex;
  align-items: center;
  margin-bottom: 41px;
}
/* channel content */
.channel_content {
  display: flex;
  align-items: center;
  margin-right: 41px;
}
.channel_main_info {
  display: flex;
  flex-direction: column;
  margin-left: 40px;
}
.channel_main_name {
  font-weight: 400;
  font-size: 38px;
}
.channel_main_views {
  font-weight: 400;
  font-size: 26px;
}

.channel_subscribe {
  font-weight: 400;
  font-size: 23px;
  background: linear-gradient(
    182.53deg,
    rgba(234, 0, 213, 0.3) 3.75%,
    rgba(61, 94, 255, 0.3) 56.09%,
    rgba(0, 234, 242, 0.3) 102.36%
  );
  border-radius: 6.0058px;
  padding: 12px;
  text-transform: uppercase;
  margin-right: 40px;
}

.channel_base_info {
  padding: 15px 25px;
  text-align: center;
  background: rgba(255, 255, 255, 0.05);
  box-shadow: inset 3.63884px 3.63884px 24.5622px rgba(255, 255, 255, 0.04);
  backdrop-filter: blur(47.1803px);
}
.channel_base_info:not(:last-child) {
  margin-right: 22px;
}
.channel_value {
  font-weight: 400;
  font-size: 23px;
}
.channel_key {
  font-weight: 400;
  font-size: 18px;
}
.playlist_content {
  width: 40%;
  display: flex;
  flex-direction: column;
  background: rgba(0, 0, 0, 0.35);
  backdrop-filter: blur(10px);
  padding-left: 8px;
  /* overflow-y: scroll; */
}
.lines_content {
  display: flex;
  align-items: center;
  width: 100%;
  height: 99px;
  margin-bottom: 65px;
}
.line_btn {
  height: 100%;
  cursor: pointer;
  width: 33.3%;
  display: flex;
  align-items: center;
  justify-content: center;
  border: 1px solid rgba(85, 85, 85, 0.14);
}
.active {
  background: linear-gradient(
    273.52deg,
    rgba(0, 234, 242, 0.2) -54.44%,
    rgba(234, 0, 213, 0.2) 110.67%
  );
  backdrop-filter: blur(10px);
}
.line_title {
  font-weight: 400;
  font-size: 27px;
  margin-left: 25px;
}

.recomends_video {
  display: flex;
  margin-bottom: 25px;

  &_wrap {
    height: calc(100vh - 300px);
    overflow-x: scroll;
  }

  img {
    aspect-ratio: 16/9;
  }
}
.recomends_video_info {
  margin-left: 27px;
}
.recomend_title {
  font-weight: 400;
  font-size: 23px;
  margin-bottom: 15px;
  padding-right: 30px;
}
.recomend_author {
  font-weight: 400;
  font-size: 23.5433px;
  color: #b1b1b1;
}

.comments_content {
  padding: 0 52px;
}

@media (max-width: 2400px) {
  .video_name {
    font-size: 24px;
  }
  .headers_content {
    padding: 50px 30px 0 30px;
  }
  .lines_content {
    height: 80px;
    margin-bottom: 40px;

    img {
      width: 30px;
    }
  }
  .line_title {
    font-size: 24px;
  }
  .recomend_title {
    font-size: 20px;
    margin-bottom: 12px;
  }
  .recomends_video_info {
    margin-left: 15px;
  }
  .video_box {
    margin-bottom: 32px;
  }
  .video_info_box {
    padding-left: 30px;
  }
  .channel_main_info {
    margin-left: 20px;
  }
  .channel_main_name {
    font-size: 32px;
  }
  .channel_main_views {
    font-size: 18px;
  }
  .channel_content {
    img {
      width: 70px;
    }
  }
}
@media (max-width: 2000px) {
  .video_name {
    font-size: 20px;
  }
  .headers_content {
    padding: 40px 20px 0 20px;
  }
  .lines_content {
    height: 60px;
    margin-bottom: 30px;

    img {
      width: 20px;
    }
  }
  .line_title {
    font-size: 20px;
  }
  .recomend_title {
    font-size: 18px;
    margin-bottom: 8px;
  }
  .recomends_video_info {
    margin-left: 12px;
  }
  .video_box {
    margin-bottom: 24px;
  }
  .video_info_box {
    padding-left: 24px;
  }
  .comment_content {
    bottom: 20px;
    right: 16px;
  }
  .comment_name {
    font-size: 14px;
    padding: 8px 20px;
  }
  .recomends_video_wrap {
    height: calc(100vh - 260px);
  }
  .recomends_video img {
    max-width: 220px;
  }
  .recomend_author {
    font-size: 18px;
  }
  .video_views_count {
    font-size: 16px;
  }
}
@media (max-width: 2000px) {
  .video_content {
    width: 55%;
    height: calc(100vh - 160px);
  }
  .playlist_content {
    width: 45%;
  }
  .recomends_video img {
    max-width: 180px;
  }
  .video_name {
    font-size: 18px;
  }
  .video_main_name {
    font-size: 24px;
  }
  .recomend_title {
    font-size: 16px;
  }
  .headers_content {
    display: none;
  }
  .recomends_video {
    margin-bottom: 8px;
  }
  .lines_content {
    height: 50px;
    margin-bottom: 20px;
  }
  .line_title {
    font-size: 18px;
    margin-left: 12px;
  }
  .channel_main_info {
    margin-left: 12px;
  }
  .channel_main_name {
    font-size: 24px;
  }
  .channel_main_views {
    font-size: 14px;
  }
  .channel_content {
    img {
      width: 50px;
    }
  }
  .channel_subscribe {
    font-size: 16px;
    padding: 10px;
    margin-right: 20px;
  }
  .channel_base_info {
    margin-right: 8px;
    padding: 12px;

    .channel_value {
      font-size: 16px;
    }
    .channel_key {
      font-size: 14px;
    }
  }
  .channel_info {
    margin-bottom: 20px;
  }
  .comments_content {
    padding: 0 30px;
  }
  .comments {
    font-size: 14px;
  }
  .recomends_video_wrap{
    height: calc(100vh - 215px);
  }
}
@media (max-width: 1600px) {
  .recomends_video_wrap{
    height: calc(100vh - 200px);
  }
  .video_content {
    height: calc(100vh - 150px);
  }
}
.slide-fade-enter-active {
  transition: all .3s ease;
}
.slide-fade-leave-active {
  transition: all .8s cubic-bezier(1.0, 0.5, 0.8, 1.0);
}
.slide-fade-enter, .slide-fade-leave-to
  /* .slide-fade-leave-active до версии 2.1.8 */ {
  transform: translateX(10px);
  opacity: 0;
}
</style>
  