<template>
  <div class="comments_comment comment">
    <img v-bind:src="$props.image" alt="comment" class="comment_img">
    <div class="comment_info">
      <div class="comment_info_header">
        <div class="comment_name">
          {{$props.name}}
        </div>
        <span class="comment_date">
                    {{$props.date}}
                  </span>
      </div>
      <div class="comment_info_text">
        {{$props.text}}
      </div>
    </div>
  </div>
</template>

<script>
export default{
  props:{
    image: [String],
    name: [String],
    text: [String],
    date: [String]
  },
  // mounted() {
  //   console.log(this.image)
  //   console.log(this.name)
  //   console.log(this.text)
  //   console.log(this.date)
  // }
}
</script>

<style lang="scss">
.comments {
    font-weight: 400;
    font-size: 24px;

  &_main {
     padding: 30px;
   }

  .comment {
    display: flex;
    align-items: flex-start;
    margin-bottom: 10px;

  &_img {
     width: 70px;
     height: 70px;
     border-radius: 50%;
   }
  &_info {
  &_header {
     display: flex;
     align-items: center;
   }
  &_text {
     font-size: 23px;
    padding-left: 10px;
   }
  }
  &_name {
     color: #01EAF2;
     font-size: 23px;
     margin-right:18px;
   }
  &_date {
     color: #82868D;
     font-size: 16px;
   }
}

&_comment {
   display: flex;
 }
}
</style>