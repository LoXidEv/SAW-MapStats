<script setup>
import '@mdui/icons/people.js';
import '@mdui/icons/monetization-on.js';
import '@mdui/icons/diamond.js';
import '@mdui/icons/task.js';
import '@mdui/icons/dashboard.js';
import '@mdui/icons/shopping-cart.js';
import '@mdui/icons/settings.js';
import '@mdui/icons/logout.js';
</script>

<template>
  <div class="bos_background_container">
    <img src="/image/background.png" alt="BananOS" class="bos_background">
    <main class="bos_container">
      <div class="bos_navbar">
        <div class="bos_header">
          <div class="bos_title">BananOS</div>
          <div class="bos_subtitle">欢迎来到超级动物世界！</div>
        </div>
        <div>
          <div class="bos_user">
            <div class="bos_friends" style="padding: 4px 20px 4px 20px;">
              <mdui-icon-people style="font-size: 30px;margin-right: 20px;"></mdui-icon-people>
              <div class="bos_content">
                <div class="bos_name">
                  社交
                </div>
                <div class="bos_number">
                  100 在线
                </div>
              </div>
            </div>
            <div class="bos_friends" style="padding: 4px 6px 4px 20px;">
              <div>
                <div class="bos_name">LoXi</div>
                <div class="bos_number">Lvl 2000 <span
                    style="display: inline-block;background-color: var(--theme-color);width: 100px;border-radius: var(--border-radius);height: 8px;margin: 0 6px 0 4px;"></span>
                </div>
              </div>
              <div style="position: relative;display: flex;justify-content: center;align-items: center;">
                <img src="https://q.qlogo.cn/headimg_dl?dst_uin=2647130977&spec=640&img_type=jpg" class="bos_avatar"
                  alt="Avatar">
                <span
                  style="position: absolute;bottom: 0;left: 0;background-color: #19ff19;border-radius: 50%;width: 10px;height: 10px;"></span>
              </div>
            </div>
          </div>
          <div class="bos_asset">
            <div class="bos_asset_content"><mdui-icon-monetization-on></mdui-icon-monetization-on>
              20,000
            </div>
            <div class="bos_asset_content"><mdui-icon-diamond></mdui-icon-diamond>2,000</div>
          </div>
        </div>
      </div>
      <div class="bos_main">
        <div class="bos_task">
          <div class="bos_task_title">
            <div style="display: flex;justify-content: start;align-items: center;gap: 8px;">
              <div class="bos_icon">
                <mdui-icon-people style="font-size: 24px; "></mdui-icon-people>
              </div>
              <div class="bos_name">组队</div>
            </div>
          </div>
          <div style="display: grid;grid-template-columns: repeat(2,1fr);gap: 10px;margin-top: 10px;">
            <div style="background-color:#2a2f36;height: 200px;width: 100%;border-radius: 20px;"></div>
            <div style="background-color:#2a2f36;height: 200px;width: 100%;border-radius: 20px;"></div>
            <div style="background-color:#2a2f36;height: 200px;width: 100%;border-radius: 20px;"></div>
            <div style="background-color:#2a2f36;height: 200px;width: 100%;border-radius: 20px;"></div>
          </div>
        </div>
        <div style="display: flex;flex-direction: column;gap: 20px;">
          <div style="display: grid;grid-template-columns: repeat(2, 1fr);gap: 40px;">
            <div class="bos_task">
              <div style="display: flex;justify-content: start;align-items: center;gap: 8px;">
                <div class="bos_icon">
                  <mdui-icon-task style="font-size: 24px; "></mdui-icon-task>
                </div>
                <div class="bos_name">任务</div>
              </div>
              <div style="margin-top: 10px;">
                <div style="background-color:#2a2f36;height: 100px;width: 100%;border-radius: 20px;"></div>
              </div>
            </div>
            <div class="bos_task">
              <div style="display: flex;justify-content: start;align-items: center;gap: 8px;">
                <div class="bos_icon">
                  <mdui-icon-dashboard style="font-size: 24px; "></mdui-icon-dashboard>
                </div>
                <div class="bos_name">挑战</div>
              </div>
              <div style="margin-top: 10px;">
                <div style="background-color:#2a2f36;height: 100px;width: 100%;border-radius: 20px;"></div>
              </div>
            </div>
          </div>
          <div class="bos_ticket">
            <img src="https://loxi.work/img/friends/th.webp"
              style="width: 100%;height: 100%;object-fit: cover;border-radius: 20px;">
          </div>
        </div>
        <div style="display: flex;flex-direction: column;gap: 20px;">
          <div class="bos_ticket">
            <img src="https://loxi.work/img/friends/th.webp"
              style="width: 100%;height: 100%;object-fit: cover;border-radius: 20px;">
          </div>
          <div style="display: flex;justify-content: center;align-items: center;gap: 20px;">
            <div class="bos_task">
              <div style="display: flex;justify-content: start;align-items: center;gap: 8px;">
                <div class="bos_icon">
                  <mdui-icon-shopping-cart style="font-size: 24px;"></mdui-icon-shopping-cart>
                </div>
                <div class="bos_name">商店</div>
              </div>
              <div style="margin-top: 10px;">
                <div style="background-color:#2a2f36;height: 100px;width: 100%;border-radius: 20px;"></div>
              </div>
            </div>
            <div class="bos_setting">
              <div class="bos_task" style="margin-bottom: 20px;">
                <div style="display: flex;justify-content: start;align-items: center;gap: 8px;">
                  <div class="bos_icon">
                    <mdui-icon-settings style="font-size: 24px;"></mdui-icon-settings>
                  </div>
                  <div class="bos_name">游戏设置选项</div>
                </div>
              </div>
              <div class="bos_task">
                <div style="display: flex;justify-content: start;align-items: center;gap: 8px;">
                  <div class="bos_icon">
                    <mdui-icon-logout style="font-size: 24px;"></mdui-icon-logout>
                  </div>
                  <div class="bos_name">退出至主菜单</div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="bos_footer">

      </div>
    </main>
  </div>
</template>

<style scoped>
.bos_task_title {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.bos_task {
  padding: 12px;
  width: 100%;
  /* height: 100%; */
  background-color: var(--background-color);
  border-radius: 30px;
}

.bos_ticket {
  border: 10px var(--background-color) solid;
  width: 100%;
  height: 100%;
  border-radius: 30px;
}

.bos_main {
  margin: 40px 0;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 50px;
}

.bos_asset_content {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 4px;
  font-size: 14px;
}

.bos_asset {
  margin-top: 8px;
  display: flex;
  justify-content: end;
  align-items: center;
  gap: 8px;
  margin-right: 30px;
}

.bos_avatar {
  width: 40px;
  height: 40px;
  border-radius: 50%;
}

.bos_name {
  font-size: 14px;
}

.bos_number {
  font-size: 12px;
}

.bos_icon {
  color: var(--icon-color);
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: #41454a;
  border-radius: 50%;
  padding: 6px;
}

.bos_friends {
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: var(--background-color);
  border-radius: var(--border-radius);
}

.bos_user {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 8px;
}

.bos_subtitle {
  opacity: 0.6;
  line-height: 1;
  letter-spacing: 1px;
}

.bos_title {
  font-family: 'Poppins SemiBold';
  font-size: 48px;
  line-height: 1.2;
}

.bos_navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.bos_container {
  padding: 60px;
  position: relative;
  display: flex;
  flex-direction: column;
  height: 100%;
  z-index: 9999;
  background-color: var(--background-color-oc);
  backdrop-filter: blur(6px);
}

.bos_background_container {
  position: relative;
  height: 100vh;
}

.bos_background {
  position: absolute;
  z-index: -1;
  height: 100%;
  width: 100%;
  object-fit: cover;
}
</style>
