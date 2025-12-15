<template>
  <footer id="footer" class="footer">
    <div class="container">
      <div class="footer-box">
        <a href="/" class="footer-logo logo">
          <img src="../assets/images/logo.png" alt="logo" />
        </a>
        <div class="footer-nav">
          <ul>
            <li>
              <a href="./goods.html"> For Restaurants </a>
            </li>
            <li>
              <a href="./goods.html"> For Couriers </a>
            </li>
            <li>
              <a href="./goods.html"> Pressroom </a>
            </li>
            <li>
              <a href="./goods.html"> Contacts </a>
            </li>
          </ul>
        </div>
        <div class="footer-social">
          <img src="../assets/images/social/INST.png" alt="instagram" />
          <img src="../assets/images/social/FB.png" alt="facebook" />
          <img src="../assets/images/social/VK.png" alt="VK" />
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {};
</script>

<style scoped>
.footer {
  min-height: 156px;
  display: flex;
  align-items: center;
  padding: 60px 0;
}

.footer-box {
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 36px;
  flex-wrap: wrap;
}

.footer-nav {
  flex-grow: 1;
}

.footer-nav ul {
  display: flex;
  align-items: center;
  list-style: none;
  padding: 0;
  margin: 0;
  gap: 15px;
  flex-wrap: wrap;
}

.footer-nav ul li {
  font-weight: 400;
  font-size: 18px;
  letter-spacing: 0%;
  color: #595959;
}

.footer-nav a {
  text-decoration: none;
}

.footer-social {
  display: flex;
  align-items: center;
  justify-content: flex-end;
  gap: 20px;
}
</style>
