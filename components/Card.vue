<template>
  <div>
    <div class="vx-card mt-base">
      <div class="card-body">
        <div>
          <div class="post-header flex mb-4 justify-between">
            <div class="items-center flex">
              <div>
                <vs-avatar class="align-items-none">
                  <img src="../assets/avatar-4.png" alt="" />
                </vs-avatar>
              </div>
              <div class="ml-4">
                <h4>{{ item.u_name }}</h4>
                <small>{{ moment(item.p_created).fromNow() }}</small>
              </div>
            </div>
            <div class="flex">
              <span class="ml-4 ">
                <vs-button transparent circle icon color="#000">
                  jknk
                </vs-button>
              </span>
            </div>
          </div>
          <div class="post-content">
            <p>{{ item.p_content }}</p>
          </div>
          <div class="post-media-container mb-6 mt-4">
            <ul class="flex post-media-list">
              <li class="post-media w-full">
                <img
                  :src="item.p_image"
                  alt="user-upload"
                  class="responsive rounded"
                />
              </li>
            </ul>
          </div>
          <div>
            <div class="flex justify-between">
              <div class="flex items-center">
                <div class="pr-30">
                  <div
                    class="flex items-center pointer underline "
                    @click="active = !active"
                  >
                    <span class="pr-5">ถูกใจ</span>
                    <span>{{ item.p_like }}</span>
                  </div>
                </div>
                <div class="flex items-center pointer underline">
                  <span class="pr-5">ความคิดเห็น</span>
                  <span class="pr-5">{{ item.p_comment }}</span>
                  <span>รายการ</span>
                </div>
              </div>
              <div class="flex items-center">
                <vs-button transparent dark circle icon>
                  icon
                </vs-button>
              </div>
            </div>
            <!-- <div class="comments-container mt-4">
            <ul class="user-comments-list">
              <li class="commented-user flex">
                <div class="mr-3">
                  <vs-avatar circle size="40" class="align-items-none">
                    <img :src="item.p_image" alt="" />
                  </vs-avatar>
                </div>
                <div>
                  <div class="leading-tight">
                    <p class="font-medium">
                      ffdgdfgfdghfdgdfgdfgdfgdfgfd
                    </p>
                    <span class="text-xs"
                      >เตรียมพบกับ!! อีกหนึ่งบริการห้องสมุดกลาง สํานักวิทยบริการ
                      ม.อุบลฯ ความบันเทิงและความรู้ ในรูปแบบของ edutainment
                      จะดูหนัง เล่นเกมส์ ผ่อนคลายได้ที่นี่ โดย ดร.ภาคภูมิ
                      สืบนุการ ผอ.สำนักวิทยบริการ เผย เพียงเริ่มต้นเท่านั้น มี
                      ipad pro บริการ 20 เครื่อง
                      พร้อมสัมผัสสุดยอดประสบการณ์ในการเล่นเกมส์!
                      เพลิดเพลินไปกับเกมเอ็กซ์คลูซีฟสำหรับ PlayStation 4
                      บริการประมาณกลางสิงหาคมนี้</span
                    >
                  </div>
                </div>
              </li>
            </ul>
          </div>
          <div class="post-comment mt-4">
            <div class="vs-component vs-con-textarea mb-2 vs-textarea-primary">
              <textarea
                class="vs-textarea"
                placeholder="แสดงความคิดเห็น..."
              ></textarea>
            </div>
            <vs-button>
              บันทึกโพสต์
            </vs-button>
          </div> -->
          </div>
        </div>
      </div>
    </div>

    <vs-dialog not-close overflow-hidden width="400px" v-model="active">
      <template #header>
        <h4 class="not-margin">คนที่ถูกใจ</h4>
      </template>
      <div>
        <listLike />
      </div>
    </vs-dialog>
  </div>
</template>
<script>
import moment from "moment";
import ListLike from "~/components/ListLike";
export default {
  components: {
    ListLike
  },
  data() {
    return {
      active: false,
      moment: moment,
      data: null
    };
  },
  props: ["item"]
};
</script>
<style>
.vx-card {
  background: #fff;
  border-radius: 0.5rem;
  box-shadow: 0 4px 25px 0 rgba(0, 0, 0, 0.1);
  /* -webkit-transition: all 0.3s ease-in-out; */
}
.card-body {
  padding: 1.5rem;
}
.mt-base {
  margin-top: 2.2rem !important;
}
.flex {
  display: flex !important;
}
.post-content {
  word-wrap: break-word;
}
.mb-4 {
  margin-bottom: 1rem !important;
}
.justify-between {
  -webkit-box-pack: justify !important;
  -ms-flex-pack: justify !important;
  justify-content: space-between !important;
}
.pointer {
  cursor: pointer;
}
.underline:hover {
  text-decoration: underline;
}
.items-center {
  -webkit-box-align: center !important;
  -ms-flex-align: center !important;
  align-items: center !important;
}
.vs-avatar {
  align-items: unset !important;
}
.ml-4 {
  margin-left: 1rem !important;
}
.mb-6 {
  margin-bottom: 1.5rem !important;
}

.mt-4 {
  margin-top: 1rem !important;
}
ul {
  margin: 0;
  padding: 0;
}
.pl-15 {
  padding-left: 15px;
}
.pr-30 {
  padding-right: 30px;
}
.pr-5 {
  padding-right: 5px;
}
ol,
ul {
  list-style-type: none;
}
.m-1 {
  margin: 0.25rem !important;
}
.w-full {
  width: 100% !important;
}
.rounded {
  border-radius: 0.25rem !important;
}
.responsive {
  width: 100%;
  height: auto;
}
img {
  display: block;
}
.mr-3 {
  margin-right: 0.75rem !important;
}
.leading-tight {
  line-height: 1.25 !important;
  word-break: break-word;
}
.font-medium {
  font-weight: 500 !important;
}
.text-xs {
  font-size: 0.8rem !important;
}
.mb-2 {
  margin-bottom: 0.5rem !important;
}
.vs-con-textarea {
  border: 1px solid rgba(0, 0, 0, 0.2) !important;
}
.vs-con-textarea {
  width: 100%;
  position: relative;
  /* border: 1px solid rgba(0,0,0,.08); */
  /* -webkit-box-shadow: 0 0 0 0 transparent; */
  box-shadow: 0 0 0 0 transparent;
  border-radius: 6px;
  /* -webkit-transition: boxShadow .25s ease,border .25s ease,-webkit-transform .25s ease; */
  /* transition: boxShadow .25s ease,border .25s ease,-webkit-transform .25s ease;
    transition: boxShadow .25s ease,border .25s ease,transform .25s ease; */
  transition: boxShadow 0.25s ease, border 0.25s ease, transform 0.25s ease,
    -webkit-transform 0.25s ease;
  /* -webkit-transform: translate(0); */
  transform: translate(0);
  /* margin-bottom: 16px; */
}
.vs-textarea {
  font-size: 1rem;
  color: inherit;
  font-family: Montserrat, Helvetica, Arial, sans-serif;
  line-height: 1.6;
  width: 100%;
  border-radius: 6px;
  padding: 7px;
}
.vs-button {
  --vs-button-margin: 0px;
}
</style>
