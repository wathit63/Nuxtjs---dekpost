<template>
  <div class="mt-base">
    
    <div class="items-center flex ">
      <div class="center con-avatars">
        <vs-avatar size="60">
          <img src="../assets/avatar-4.png" alt="" />
      </vs-avatar>
      </div>
      <div class="ml-4">
        <h4>Ae wathit</h4>
        <small>wathit ruchairam</small>
      </div>
    </div>
    <div class="vs-list mt-top">
      <div class="vs-list--header">
        <div class="list-titles">
          <div class="vs-list--title font-14">
            แนะนำสำหรับคุณ
          </div>
        </div>
      </div>
      <div class="vs-list--item">
        <div class="vs-list--avatar">
          <vs-avatar class="align-items-none">
            <img src="../assets/avatar-9.png" alt="" />
          </vs-avatar>
        </div>
        <div class="list-titles ml-4">
          <div class="vs-list--title">
            Ae wathit
          </div>
          <div class="vs-list--subtitle">
            4 วันที่แล้ว
          </div>
        </div>
      </div>
      <div class="vs-list--item">
        <div class="vs-list--avatar">
          <vs-avatar class="align-items-none">
            <img src="../assets/avatar-5.png" alt="" />
          </vs-avatar>
        </div>
        <div class="list-titles ml-4">
          <div class="vs-list--title">
            Ae wathit
          </div>
          <div class="vs-list--subtitle">
            4 วันที่แล้ว
          </div>
        </div>
      </div>
      <div class="vs-list--item">
        <div class="vs-list--avatar">
          <vs-avatar class="align-items-none">
            <img src="../assets/avatar-9.png" alt="" />
          </vs-avatar>
        </div>
        <div class="list-titles ml-4">
          <div class="vs-list--title">
            Ae wathit
          </div>
          <div class="vs-list--subtitle">
            4 วันที่แล้ว
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<style>
.flex {
  display: flex !important;
}
.ml-4 {
  margin-left: 1rem !important;
}
.mt-base {
  margin-top: 2.2rem !important;
}
.mt-top {
  margin-top: 0.2rem !important;
}
.font-14{
    font-size: 14px;
}
.vs-list {
  width: 100%;
  position: relative;
  padding: 5px;
}
.vs-header-list-primary {
  color: rgba(var(--vs-primary), 1);
}
.items-center {
  -webkit-box-align: center !important;
  -ms-flex-align: center !important;
  align-items: center !important;
}
.vs-list--header,
.vs-list--item {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-align: center;
  -ms-flex-align: center;
  align-items: center;
  -webkit-box-pack: start;
  -ms-flex-pack: start;
  justify-content: flex-start;
}
.vs-list--header {
  padding: 8px 0;
  font-weight: 700;
  -webkit-box-shadow: 0 7px 7px -5px rgba(0, 0, 0, 0.08);
  box-shadow: 0 7px 7px -5px rgba(0, 0, 0, 0.08);
  margin-bottom: 5px;
}
.vs-list--title {
  font-weight: 600;
}
.vs-list--item {
  border-bottom: 1px solid rgba(0, 0, 0, 0.08);
  padding: 5px;
}
.vs-list--subtitle {
  font-size: 0.8rem;
}
.vs-list--item .vs-list--avatar {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-align: center;
  -ms-flex-align: center;
  align-items: center;
}
</style>
