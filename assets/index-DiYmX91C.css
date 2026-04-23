<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>远大芯科技 - 专业游戏鼠标芯片方案提供商</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif; }
        :root {
            --primary: #0066ff; --primary-dark: #0052cc; --secondary: #00d4ff; --dark: #0a0e17; --darker: #060913;
            --light: #f8f9fa; --gray: #6c757d; --card-bg: #13182b;
        }
        body { background-color: var(--dark); color: var(--light); line-height: 1.6; overflow-x: hidden; }
        .container { width: 100%; max-width: 1200px; margin: 0 auto; padding: 0 20px; }
        /* 导航栏 */
        header { background-color: rgba(10, 14, 23, 0.95); backdrop-filter: blur(10px); position: fixed; width: 100%; z-index: 1000; border-bottom: 1px solid rgba(0, 102, 255, 0.2); }
        .navbar { display: flex; justify-content: space-between; align-items: center; padding: 18px 0; }
        .logo { display: flex; align-items: center; font-size: 24px; font-weight: 700; color: white; }
        .logo i { color: var(--primary); margin-right: 10px; font-size: 28px; }
        .nav-links { display: flex; list-style: none; }
        .nav-links li { margin-left: 35px; }
        .nav-links a { color: var(--light); text-decoration: none; font-weight: 500; font-size: 16px; transition: color 0.3s; position: relative; }
        .nav-links a:hover { color: var(--secondary); }
        .nav-links a::after { content: ''; position: absolute; width: 0; height: 2px; background: var(--primary); left: 0; bottom: -5px; transition: width 0.3s; }
        .nav-links a:hover::after { width: 100%; }
        .contact-btn { background: linear-gradient(45deg, var(--primary), var(--secondary)); color: white; border: none; padding: 10px 25px; border-radius: 30px; font-weight: 600; cursor: pointer; transition: transform 0.3s, box-shadow 0.3s; }
        .contact-btn:hover { transform: translateY(-3px); box-shadow: 0 10px 20px rgba(0, 102, 255, 0.3); }
        .mobile-menu { display: none; font-size: 24px; cursor: pointer; }
        /* 英雄区域 */
        .hero { padding: 180px 0 120px; background: linear-gradient(135deg, var(--darker) 0%, var(--dark) 100%); position: relative; overflow: hidden; }
        .hero::before { content: ''; position: absolute; width: 500px; height: 500px; background: radial-gradient(circle, rgba(0, 102, 255, 0.1) 0%, transparent 70%); top: -200px; right: -100px; }
        .hero-content { display: flex; align-items: center; justify-content: space-between; }
        .hero-text { flex: 1; max-width: 600px; }
        .hero-text h1 { font-size: 48px; margin-bottom: 20px; line-height: 1.2; background: linear-gradient(to right, var(--primary), var(--secondary)); -webkit-background-clip: text; background-clip: text; color: transparent; }
        .hero-text p { font-size: 18px; color: #aaa; margin-bottom: 30px; }
        .hero-image { flex: 1; display: flex; justify-content: center; position: relative; }
        .chip-img { width: 350px; height: 350px; background: linear-gradient(45deg, var(--card-bg), #1a2342); border-radius: 20px; display: flex; align-items: center; justify-content: center; box-shadow: 0 20px 40px rgba(0, 0, 0, 0.4); position: relative; overflow: hidden; }
        .chip-img::before { content: ''; position: absolute; width: 200px; height: 200px; background: radial-gradient(circle, var(--primary) 0%, transparent 70%); filter: blur(40px); opacity: 0.3; }
        .chip-core { width: 180px; height: 180px; background-color: #0a0e17; border-radius: 50%; display: flex; align-items: center; justify-content: center; position: relative; z-index: 1; border: 2px solid rgba(0, 102, 255, 0.3); }
        .chip-core::after { content: ''; position: absolute; width: 100px; height: 100px; background-color: #00d4ff; border-radius: 50%; filter: blur(20px); opacity: 0.3; }
        .chip-text { position: absolute; color: white; font-size: 24px; font-weight: 700; z-index: 2; text-align: center; }
        .chip-text span { font-size: 14px; display: block; color: var(--secondary); font-weight: 400; }
        /* 特性区域 */
        .section-title { text-align: center; font-size: 36px; margin-bottom: 60px; color: white; }
        .section-title span { color: var(--primary); }
        .features { padding: 100px 0; background-color: var(--darker); }
        .features-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 30px; }
        .feature-card { background-color: var(--card-bg); padding: 30px; border-radius: 15px; transition: transform 0.3s, box-shadow 0.3s; border: 1px solid rgba(0, 102, 255, 0.1); }
        .feature-card:hover { transform: translateY(-10px); box-shadow: 0 15px 30px rgba(0, 0, 0, 0.3); border-color: rgba(0, 102, 255, 0.3); }
        .feature-icon { width: 70px; height: 70px; background: linear-gradient(45deg, var(--primary), var(--secondary)); border-radius: 50%; display: flex; align-items: center; justify-content: center; margin-bottom: 20px; font-size: 28px; }
        .feature-card h3 { font-size: 22px; margin-bottom: 15px; color: white; }
        .feature-card p { color: #aaa; }
        /* 产品方案区域 */
        .solutions { padding: 100px 0; background-color: var(--dark); }
        .solutions-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 30px; }
        .solution-card { background-color: var(--card-bg); border-radius: 15px; overflow: hidden; transition: transform 0.3s; }
        .solution-card:hover { transform: translateY(-10px); }
        .solution-img { height: 200px; background: linear-gradient(45deg, #1a2342, #0a0e17); display: flex; align-items: center; justify-content: center; font-size: 60px; color: var(--primary); }
        .solution-content { padding: 25px; }
        .solution-content h3 { font-size: 22px; margin-bottom: 15px; color: white; }
        .solution-content ul { list-style: none; margin-top: 15px; }
        .solution-content li { margin-bottom: 8px; color: #aaa; padding-left: 25px; position: relative; }
        .solution-content li::before { content: '✓'; position: absolute; left: 0; color: var(--secondary); font-weight: bold; }
        /* 关于我们区域 */
        .about { padding: 100px 0; background-color: var(--darker); }
        .about-content { display: flex; align-items: center; justify-content: space-between; gap: 50px; }
        .about-text { flex: 1; }
        .about-text h2 { font-size: 36px; margin-bottom: 20px; color: white; }
        .about-text h2 span { color: var(--primary); }
        .about-text p { margin-bottom: 20px; color: #aaa; font-size: 17px; }
        .about-stats { display: flex; margin-top: 30px; gap: 30px; }
        .stat { text-align: center; }
        .stat-number { font-size: 36px; font-weight: 700; color: var(--primary); margin-bottom: 5px; }
        .stat-label { color: #aaa; font-size: 15px; }
        .about-image { flex: 1; display: flex; justify-content: center; }
        .about-chip { width: 300px; height: 300px; background: linear-gradient(45deg, var(--card-bg), #1a2342); border-radius: 20px; display: flex; align-items: center; justify-content: center; position: relative; overflow: hidden; box-shadow: 0 20px 40px rgba(0, 0, 0, 0.4); }
        .circuit { width: 100%; height: 100%; position: absolute; background-image: linear-gradient(90deg, transparent 49%, rgba(0, 102, 255, 0.2) 50%, transparent 51%), linear-gradient(transparent 49%, rgba(0, 102, 255, 0.2) 50%, transparent 51%); background-size: 40px 40px; opacity: 0.5; }
        /* 联系区域 */
        .contact { padding: 100px 0; background-color: var(--dark); text-align: center; }
        .contact h2 { font-size: 36px; margin-bottom: 15px; color: white; }
        .contact p { color: #aaa; font-size: 18px; max-width: 700px; margin: 0 auto 40px; }
        .contact-info { display: flex; justify-content: center; flex-wrap: wrap; gap: 40px; margin-bottom: 50px; }
        .contact-item { display: flex; align-items: center; gap: 15px; }
        .contact-icon { width: 50px; height: 50px; background: linear-gradient(45deg, var(--primary), var(--secondary)); border-radius: 50%; display: flex; align-items: center; justify-content: center; font-size: 20px; }
        .contact-details h4 { font-size: 18px; margin-bottom: 5px; color: white; }
        .contact-details p { margin: 0; font-size: 16px; color: #aaa; }
        /* 页脚 */
        footer { background-color: var(--darker); padding: 50px 0 20px; border-top: 1px solid rgba(255, 255, 255, 0.05); }
        .footer-content { display: flex; justify-content: space-between; flex-wrap: wrap; gap: 40px; margin-bottom: 30px; }
        .footer-logo { flex: 1; min-width: 250px; }
        .footer-links { flex: 1; min-width: 200px; }
        .footer-links h4 { font-size: 20px; margin-bottom: 20px; color: white; }
        .footer-links ul { list-style: none; }
        .footer-links li { margin-bottom: 12px; }
        .footer-links a { color: #aaa; text-decoration: none; transition: color 0.3s; }
        .footer-links a:hover { color: var(--primary); }
        .copyright { text-align: center; padding-top: 20px; border-top: 1px solid rgba(255, 255, 255, 0.05); color: #aaa; font-size: 14px; line-height: 1.8; }
        /* 新增：备案信息样式 */
        .beian { margin-top: 10px; }
        .beian a { color: #8a9ba8; text-decoration: none; transition: color 0.3s; font-size: 13px; }
        .beian a:hover { color: var(--secondary); text-decoration: underline; }
        .beian i { margin-right: 5px; font-size: 12px; }
        /* 响应式设计 */
        @media (max-width: 992px) {
            .hero-content { flex-direction: column; text-align: center; }
            .hero-text { margin-bottom: 50px; }
            .hero-text h1 { font-size: 40px; }
            .about-content { flex-direction: column; }
        }
        @media (max-width: 768px) {
            .nav-links { display: none; }
            .mobile-menu { display: block; }
            .hero { padding: 150px 0 80px; }
            .hero-text h1 { font-size: 32px; }
            .section-title { font-size: 30px; }
            .contact-info { flex-direction: column; align-items: center; }
            .footer-content { flex-direction: column; }
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <nav class="navbar">
                <div class="logo"><i class="fas fa-microchip"></i><span>远大芯科技</span></div>
                <ul class="nav-links">
                    <li><a href="#home">首页</a></li><li><a href="#features">核心技术</a></li>
                    <li><a href="#solutions">产品方案</a></li><li><a href="#about">关于我们</a></li>
                    <li><a href="#contact">联系我们</a></li>
                </ul>
                <button class="contact-btn">获取方案</button>
                <div class="mobile-menu"><i class="fas fa-bars"></i></div>
            </nav>
        </div>
    </header>
    <section class="hero" id="home">
        <div class="container">
            <div class="hero-content">
                <div class="hero-text">
                    <h1>引领游戏鼠标芯片技术革新</h1>
                    <p>深圳市远大芯科技有限公司专注于高性能游戏鼠标芯片解决方案，提供从传感器、微处理器到无线连接的一站式芯片方案，为全球游戏外设品牌提供核心技术支持。</p>
                    <button class="contact-btn">立即咨询方案</button>
                </div>
                <div class="hero-image">
                    <div class="chip-img">
                        <div class="chip-core">
                            <div class="chip-text">YDX-8800<span>游戏鼠标专用芯片</span></div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
    <section class="features" id="features">
        <div class="container">
            <h2 class="section-title">核心<span>技术</span></h2>
            <div class="features-grid">
                <div class="feature-card">
                    <div class="feature-icon"><i class="fas fa-bullseye"></i></div>
                    <h3>高精度传感器</h3>
                    <p>自主研发的PMW系列光学传感器，最高可达26000 DPI，追踪速度650 IPS，精度达99.8%，零平滑、零抖动。</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon"><i class="fas fa-tachometer-alt"></i></div>
                    <h3>超低延迟处理</h3>
                    <p>采用32位ARM Cortex-M4内核，主频高达200MHz，响应时间低于1ms，确保游戏操作的即时反馈。</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon"><i class="fas fa-bluetooth"></i></div>
                    <h3>智能无线连接</h3>
                    <p>支持2.4G/蓝牙5.2双模连接，智能抗干扰技术，续航时间长达150小时，充电仅需15分钟。</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon"><i class="fas fa-cogs"></i></div>
                    <h3>可编程引擎</h3>
                    <p>提供完整的SDK开发工具包，支持按键自定义、RGB灯光控制、宏编程等功能，满足个性化需求。</p>
                </div>
            </div>
        </div>
    </section>
    <section class="solutions" id="solutions">
        <div class="container">
            <h2 class="section-title">产品<span>方案</span></h2>
            <div class="solutions-grid">
                <div class="solution-card">
                    <div class="solution-img"><i class="fas fa-gamepad"></i></div>
                    <div class="solution-content">
                        <h3>旗舰竞技方案</h3>
                        <p>为职业电竞选手设计的高性能解决方案，极致性能与稳定性结合。</p>
                        <ul>
                            <li>YDX-8800旗舰传感器</li><li>4000Hz回报率</li>
                            <li>光学微动开关</li><li>8个可编程按键</li><li>256KB板载内存</li>
                        </ul>
                    </div>
                </div>
                <div class="solution-card">
                    <div class="solution-img"><i class="fas fa-wifi"></i></div>
                    <div class="solution-content">
                        <h3>无线游戏方案</h3>
                        <p>专为无线游戏鼠标设计的低功耗高性能解决方案。</p>
                        <ul>
                            <li>YDX-6800无线传感器</li><li>2.4G/蓝牙双模</li>
                            <li>100小时续航</li><li>快速充电技术</li><li>抗干扰技术</li>
                        </ul>
                    </div>
                </div>
                <div class="solution-card">
                    <div class="solution-img"><i class="fas fa-dollar-sign"></i></div>
                    <div class="solution-content">
                        <h3>高性价比方案</h3>
                        <p>为大众市场设计的高性能成本效益解决方案。</p>
                        <ul>
                            <li>YDX-4800入门传感器</li><li>1000Hz回报率</li>
                            <li>6个可编程按键</li><li>RGB灯光控制</li><li>完整的SDK支持</li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </section>
    <section class="about" id="about">
        <div class="container">
            <div class="about-content">
                <div class="about-text">
                    <h2>关于<span>远大芯</span></h2>
                    <p>深圳市远大芯科技有限公司成立于2015年，专注于游戏外设芯片解决方案的研发与创新。公司总部位于深圳高新科技园，拥有超过100名研发工程师，其中博士、硕士占比超过40%。</p>
                    <p>我们与全球多家知名游戏外设品牌建立了长期合作关系，年出货芯片超过2000万片，市场份额位居行业前列。公司已获得ISO9001质量管理体系认证，拥有50多项核心专利技术。</p>
                    <p>未来，我们将继续深耕游戏外设芯片领域，推动技术创新，为全球玩家提供更卓越的游戏体验。</p>
                    <div class="about-stats">
                        <div class="stat"><div class="stat-number">8年</div><div class="stat-label">行业经验</div></div>
                        <div class="stat"><div class="stat-number">50+</div><div class="stat-label">专利技术</div></div>
                        <div class="stat"><div class="stat-number">2000万+</div><div class="stat-label">年出货量</div></div>
                        <div class="stat"><div class="stat-number">100+</div><div class="stat-label">研发团队</div></div>
                    </div>
                </div>
                <div class="about-image">
                    <div class="about-chip">
                        <div class="circuit"></div>
                        <div class="chip-text" style="font-size: 20px;">创新驱动<br><span>技术领先</span></div>
                    </div>
                </div>
            </div>
        </div>
    </section>
    <section class="contact" id="contact">
        <div class="container">
            <h2>联系我们</h2>
            <p>如果您对我们的芯片方案感兴趣，或需要定制化的解决方案，请随时与我们联系。我们的技术团队将在24小时内回复您的咨询。</p>
            <div class="contact-info">
                <div class="contact-item">
                    <div class="contact-icon"><i class="fas fa-map-marker-alt"></i></div>
                    <div class="contact-details"><h4>公司地址</h4><p>广东省深圳市南山区珠光路东200米珠光创新科技园1栋505</p></div>
                </div>
                <div class="contact-item">
                    <div class="contact-icon"><i class="fas fa-phone"></i></div>
                    <div class="contact-details"><h4>联系电话</h4><p>0755-86070203</p></div>
                </div>
                <div class="contact-item">
                    <div class="contact-icon"><i class="fas fa-envelope"></i></div>
                    <div class="contact-details"><h4>电子邮箱</h4><p>sales@yuandaxin.com</p></div>
                </div>
            </div>
            <button class="contact-btn">获取定制方案</button>
        </div>
    </section>
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-logo">
                    <div class="logo"><i class="fas fa-microchip"></i><span>远大芯科技</span></div>
                    <p style="margin-top: 20px; color: #aaa; max-width: 300px;">专注于游戏鼠标芯片解决方案，为全球游戏外设品牌提供核心技术支持。</p>
                </div>
                <div class="footer-links">
                    <h4>快速链接</h4>
                    <ul>
                        <li><a href="#home">首页</a></li><li><a href="#features">核心技术</a></li>
                        <li><a href="#solutions">产品方案</a></li><li><a href="#about">关于我们</a></li>
                        <li><a href="#contact">联系我们</a></li>
                    </ul>
                </div>
                <div class="footer-links">
                    <h4>产品方案</h4>
                    <ul>
                        <li><a href="#">旗舰竞技方案</a></li><li><a href="#">无线游戏方案</a></li>
                        <li><a href="#">高性价比方案</a></li><li><a href="#">定制化方案</a></li>
                    </ul>
                </div>
                <div class="footer-links">
                    <h4>关注我们</h4>
                    <ul>
                        <li><a href="#"><i class="fab fa-weixin" style="margin-right: 8px;"></i>微信公众号</a></li>
                        <li><a href="#"><i class="fab fa-linkedin" style="margin-right: 8px;"></i>LinkedIn</a></li>
                        <li><a href="#"><i class="fab fa-github" style="margin-right: 8px;"></i>GitHub</a></li>
                        <li><a href="#"><i class="fas fa-rss" style="margin-right: 8px;"></i>技术博客</a></li>
                    </ul>
                </div>
            </div>
            <!-- 这里是新增的备案信息部分 -->
            <div class="copyright">
                <p>© 2023 深圳市远大芯科技有限公司 版权所有 粤ICP备2021061140号-1</p>
                <div class="beian">
                    <!-- 这里使用了您指定的正确备案号链接 -->
                    <a href="https://beian.miit.gov.cn" target="_blank" rel="noopener">
                        <i class="fas fa-link"></i>粤ICP备2021061140号-1
                    </a>
                </div>
            </div>
        </div>
    </footer>
    <script>
        window.addEventListener('scroll', function() {
            const header = document.querySelector('header');
            header.style.backgroundColor = window.scrollY > 50 ? 'rgba(10, 14, 23, 0.98)' : 'rgba(10, 14, 23, 0.95)';
        });
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                const targetId = this.getAttribute('href');
                if(targetId === '#') return;
                const targetElement = document.querySelector(targetId);
                if(targetElement) {
                    window.scrollTo({ top: targetElement.offsetTop - 80, behavior: 'smooth' });
                }
            });
        });
        document.querySelectorAll('.contact-btn').forEach(button => {
            button.addEventListener('click', function() {
                alert('感谢您的咨询！我们的销售团队将尽快与您联系。');
            });
        });
        const mobileMenuBtn = document.querySelector('.mobile-menu');
        const navLinks = document.querySelector('.nav-links');
        mobileMenuBtn.addEventListener('click', function() {
            navLinks.style.display = navLinks.style.display === 'flex' ? 'none' : 'flex';
        });
        window.addEventListener('resize', function() {
            navLinks.style.display = window.innerWidth > 768 ? 'flex' : 'none';
        });
    </script>
</body>
</html>