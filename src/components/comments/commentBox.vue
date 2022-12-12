<template>
  <div class="comment_box">
    <div class="comment_name">
      {{$props.name}}
    </div>
    <img
        class="comment_icon"
        v-bind:src="$props.src"
        alt=""
    />
  </div>
</template>

<script>
export default{
  props:{
    name: [String],
    src: [String]
  }
}
</script>

<style>
  .comment_box {
    display: flex;
    justify-content: flex-end;
  }

  .comment_box:not(:last-child) {
    margin-bottom: 7px;
  }
  .comment_name {
     font-weight: 400;
     font-size: 16px;
     padding: 11px 24px;
     border-radius: 10px 10px 0px 10px;
     background: rgba(0, 0, 0, 0.5);
     backdrop-filter: blur(7.5px);
     margin-right: 7px;
   }
</style>