<script setup>
import { ref } from 'vue'
import './style.css'

const menuOpen = ref(false)
const toggleMenu = () => { menuOpen.value = !menuOpen.value }
const closeMenu = () => { menuOpen.value = false }
</script>

<template>
<header>
    <div class="wrap nav">
      <a class="brand" href="#top" aria-label="红炉火锅，返回首页"><span class="brand-mark">炉</span><span>红炉火锅</span></a>
      <button class="menu-toggle" type="button" :aria-label="menuOpen ? '关闭菜单' : '打开菜单'" :aria-expanded="menuOpen" aria-controls="nav-links" @click="toggleMenu">{{ menuOpen ? '×' : '☰' }}</button>
      <nav id="nav-links" class="nav-links" :class="{ open: menuOpen }" aria-label="主导航" @click="closeMenu">
        <a href="#story">关于红炉</a><a href="#broths">招牌锅底</a><a href="#menu">精选食材</a><a class="nav-cta" href="#visit">门店信息 ↗</a>
      </nav>
    </div>
  </header>
  <main id="top">
    <section class="hero" aria-labelledby="hero-title">
      <div class="wrap">
        <div class="hero-kicker">围炉而坐 · 热辣相逢</div>
        <h1 class="serif" id="hero-title">这一锅热气，<br><em>刚好是相聚。</em></h1>
        <p>好汤慢慢熬，鲜味慢慢涮。让每一次围坐，都有值得回味的热闹与温暖。</p>
        <div class="buttons"><a class="btn btn-red" href="#broths">探索招牌锅底 <span class="arrow">↗</span></a><a class="btn btn-outline" href="#menu">看看精选食材 <span class="arrow">↗</span></a></div>
      </div>
      <div class="hero-bottom"><div class="wrap"><span>HOT POT · GOOD TIMES · GOOD COMPANY</span><div><span>向下探索</span><div class="scroll-line"></div></div></div></div>
    </section>
    <section class="intro" id="story" aria-labelledby="story-title"><div class="wrap intro-grid">
      <div class="intro-text"><span class="eyebrow">OUR STORY / 红炉的心意</span><h2 class="section-title serif" id="story-title">锅里翻滚的是鲜香，<br>桌边留下的是笑声。</h2><p class="section-copy">一顿好火锅，总是从一锅认真熬煮的汤开始。红炉把浓郁与清鲜摆在同一张桌上，让喜欢热辣的你和偏爱温和的朋友，都能自在地享受这一餐。</p><div class="intro-line">把日子过得热气腾腾</div></div>
      <div class="intro-visual"><img src="/menu.png" alt="鲜切牛肉、蔬菜与菌菇组成的火锅食材拼盘" loading="lazy"><div class="seal">一锅好味<br>一桌欢聚</div></div>
    </div></section>
    <section class="feature" id="broths" aria-labelledby="broth-title"><div class="wrap">
      <div class="feature-heading"><div><span class="eyebrow">THE BROTH / 招牌锅底</span><h2 class="section-title serif" id="broth-title">先选一锅，<br>再开一场好聚会。</h2></div><p>从热烈到温润，总有一款锅底，能接住今天的胃口。</p></div>
      <div class="pot-grid"><article class="pot-card"><div class="pot-bottom"><span class="pot-icon" aria-hidden="true">火</span><span class="pot-num">01 / BOLD</span></div><div><h3>经典牛油红锅</h3><p>醇厚辛香，越涮越有滋味。给喜欢痛快热辣的人。</p></div></article><article class="pot-card"><div class="pot-bottom"><span class="pot-icon" aria-hidden="true">鲜</span><span class="pot-num">02 / GENTLE</span></div><div><h3>鲜香菌菇汤</h3><p>菌香温润，衬出食材本身的清甜与鲜美。</p></div></article><article class="pot-card"><div class="pot-bottom"><span class="pot-icon" aria-hidden="true">鸳</span><span class="pot-num">03 / TOGETHER</span></div><div><h3>鸳鸯双拼锅</h3><p>一半热烈，一半温柔。让每个人都吃得尽兴。</p></div></article></div>
    </div></section>
    <section class="menu-section" id="menu" aria-labelledby="menu-title"><div class="wrap">
      <div class="menu-head"><div><span class="eyebrow">FRESH SELECTION / 精选食材</span><h2 class="section-title serif" id="menu-title">好锅底，要配好食材。</h2></div><p class="section-copy">肉香、脆嫩与清甜交替上桌，每一筷都是火锅的高光时刻。</p></div>
      <div class="menu-layout"><div class="menu-photo"><img src="/menu.png" alt="牛肉、菌菇、蔬菜、豆腐等火锅食材" loading="lazy"></div><div><div class="menu-list"><div class="menu-item"><span class="menu-count">01</span><div><h3>鲜切牛肉</h3><p>轻涮片刻，入口柔嫩，最懂红锅的浓香。</p></div></div><div class="menu-item"><span class="menu-count">02</span><div><h3>时令鲜蔬</h3><p>一抹清爽，让一桌丰盛更加鲜活。</p></div></div><div class="menu-item"><span class="menu-count">03</span><div><h3>菌菇拼盘</h3><p>吸饱汤汁，也把自然的鲜味留在口中。</p></div></div><div class="menu-item"><span class="menu-count">04</span><div><h3>豆香小品</h3><p>软嫩与弹韧交织，是每锅都少不了的满足。</p></div></div></div><p class="menu-note">* 页面菜品为展示示例，实际供应以门店菜单为准。</p></div></div>
    </div></section>
    <section class="quote"><span class="eyebrow">A TABLE FOR TOGETHERNESS</span><h2>最好的味道，<br>是大家坐在一起的味道。</h2><p>围一炉热气，聊一晚故事。</p></section>
    <section class="visit" id="visit" aria-labelledby="visit-title"><div class="wrap visit-grid"><div><span class="eyebrow">VISIT US / 欢迎来坐坐</span><h2 class="section-title serif" id="visit-title">好好吃饭，<br>好好相聚。</h2><p class="section-copy">不管是老朋友见面，还是与家人吃顿团圆饭，红炉都为一桌热热闹闹的时光留着位置。</p></div><div><div class="info-box"><div class="info-row"><strong>门店地址</strong><span>请在此填写门店详细地址</span></div><div class="info-row"><strong>营业时间</strong><span>请在此填写实际营业时间</span></div><div class="info-row"><strong>订位联系</strong><span>请在此填写电话或订位链接</span></div></div></div></div></section>
  </main>
  <footer><div class="wrap footer-inner"><div><a class="brand" href="#top"><span class="brand-mark">炉</span><span>红炉火锅</span></a><p>热气腾腾，刚好相聚。</p></div><div class="footer-links"><a href="#story">关于红炉</a><a href="#broths">招牌锅底</a><a href="#menu">精选食材</a><a href="#visit">门店信息</a></div></div></footer>
  
</template>

