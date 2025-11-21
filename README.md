<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>你的姓名 - 个人主页</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        /* 基础样式重置 */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
            background-color: #f8f9fa;
        }

        /* 两栏布局 - 使用Flexbox实现 */
        .container {
            display: flex;
            min-height: 100vh;
        }

        /* 左侧边栏样式 */
        .sidebar {
            flex: 0 0 300px;
            background: linear-gradient(135deg, #2c3e50 0%, #3498db 100%);
            color: white;
            padding: 2rem;
            position: fixed;
            width: 300px;
            height: 100vh;
            overflow-y: auto;
        }

        .profile-image {
            text-align: center;
            margin-bottom: 1.5rem;
        }

        .profile-image img {
            width: 180px;
            height: 180px;
            border-radius: 50%;
            object-fit: cover;
            border: 5px solid rgba(255,255,255,0.2);
        }

        .contact-info {
            margin: 1.5rem 0;
        }

        .contact-item {
            display: flex;
            align-items: center;
            margin-bottom: 0.8rem;
            font-size: 0.9rem;
        }

        .contact-item i {
            width: 20px;
            margin-right: 10px;
            text-align: center;
        }

        .skills {
            margin: 1.5rem 0;
        }

        .skill-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
            margin-top: 0.5rem;
        }

        .skill-tag {
            background: rgba(255,255,255,0.2);
            padding: 0.3rem 0.8rem;
            border-radius: 15px;
            font-size: 0.8rem;
        }

        /* 右侧主内容区样式 */
        .main-content {
            flex: 1;
            margin-left: 300px;
            padding: 2rem 3rem;
            background: white;
        }

        /* 导航栏样式 */
        .navbar {
            background: white;
            padding: 1rem 0;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            position: sticky;
            top: 0;
            z-index: 100;
        }

        .nav-links {
            display: flex;
            justify-content: center;
            gap: 2rem;
        }

        .nav-link {
            color: #2c3e50;
            text-decoration: none;
            padding: 0.5rem 1rem;
            border-radius: 5px;
            transition: all 0.3s ease;
            font-weight: 500;
        }

        .nav-link:hover {
            background: #3498db;
            color: white;
        }

        /* 内容区块样式 */
        .section {
            margin-bottom: 3rem;
            padding-bottom: 1.5rem;
            border-bottom: 1px solid #eee;
        }

        .section:last-child {
            border-bottom: none;
        }

        .section h2 {
            color: #2c3e50;
            margin-bottom: 1.5rem;
            padding-bottom: 0.5rem;
            border-bottom: 2px solid #3498db;
            display: inline-block;
        }

        /* 经历时间线样式 */
        .timeline-item {
            margin-bottom: 2rem;
            padding-left: 1.5rem;
            border-left: 2px solid #3498db;
            position: relative;
        }

        .timeline-item::before {
            content: '';
            position: absolute;
            left: -8px;
            top: 0;
            width: 12px;
            height: 12px;
            border-radius: 50%;
            background: #3498db;
        }

        .timeline-date {
            color: #7f8c8d;
            font-style: italic;
            margin-bottom: 0.5rem;
        }

        /* 项目网格样式 */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 1.5rem;
            margin-top: 1.5rem;
        }

        .project-card {
            background: #f8f9fa;
            padding: 1.5rem;
            border-radius: 8px;
            border-left: 4px solid #3498db;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .project-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
        }

        /* 响应式设计 */
        @media (max-width: 768px) {
            .container {
                flex-direction: column;
            }
            
            .sidebar {
                position: static;
                width: 100%;
                height: auto;
            }
            
            .main-content {
                margin-left: 0;
                padding: 1.5rem;
            }
            
            .nav-links {
                flex-wrap: wrap;
                gap: 1rem;
            }
            
            .projects-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- 左侧边栏 - 个人信息 -->
        <aside class="sidebar">
            <div class="profile-image">
                <img src="https://via.placeholder.com/200x200/3498db/ffffff?text=Your+Photo" alt="个人照片" id="profile-pic">
            </div>
            
            <h1 id="username">你的名字</h1>
            <p class="title" id="job-title">你的职位/专业</p>
            
            <div class="contact-info">
                <div class="contact-item">
                    <i class="fas fa-envelope"></i>
                    <span id="email">your.email@example.com</span>
                </div>
                <div class="contact-item">
                    <i class="fas fa-map-marker-alt"></i>
                    <span id="location">所在城市</span>
                </div>
                <div class="contact-item">
                    <i class="fas fa-phone"></i>
                    <span id="phone">电话号码</span>
                </div>
                <div class="contact-item">
                    <i class="fab fa-github"></i>
                    <span id="github">GitHub用户名</span>
                </div>
            </div>
            
            <div class="about">
                <h3>关于我</h3>
                <p id="user-bio">这里是一段简短的自我介绍，描述你的研究兴趣、专业方向和职业目标。</p>
            </div>
            
            <div class="skills">
                <h3>研究领域</h3>
                <div class="skill-tags">
                    <span class="skill-tag">领域一</span>
                    <span class="skill-tag">领域二</span>
                    <span class="skill-tag">领域三</span>
                </div>
            </div>
            
            <div class="skills">
                <h3>技术技能</h3>
                <div class="skill-tags">
                    <span class="skill-tag">技能一</span>
                    <span class="skill-tag">技能二</span>
                    <span class="skill-tag">技能三</span>
                    <span class="skill-tag">技能四</span>
                </div>
            </div>
            
            <div class="languages">
                <h3>语言能力</h3>
                <div class="skill-tags">
                    <span class="skill-tag">中文 (母语)</span>
                    <span class="skill-tag">英语 (流利)</span>
                </div>
            </div>
        </aside>
        
        <!-- 右侧主内容区 -->
        <main class="main-content">
            <!-- 导航栏 -->
            <nav class="navbar">
                <div class="nav-links">
                    <a href="#about" class="nav-link">关于</a>
                    <a href="#education" class="nav-link">教育背景</a>
                    <a href="#research" class="nav-link">研究经历</a>
                    <a href="#publications" class="nav-link">学术成果</a>
                    <a href="#projects" class="nav-link">项目作品</a>
                    <a href="#internship" class="nav-link">实习经历</a>
                </div>
            </nav>
            
            <!-- 关于部分 -->
            <section id="about" class="section">
                <h2>关于我</h2>
                <p>在这里写一段详细的自我介绍，包括你的学术背景、研究兴趣、职业目标等。可以分成几个段落，让访问者更全面地了解你。</p>
                
                <h3>研究兴趣</h3>
                <ul>
                    <li>研究方向一</li>
                    <li>研究方向二</li>
                    <li>研究方向三</li>
                </ul>
            </section>
            
            <!-- 教育背景 -->
            <section id="education" class="section">
                <h2>教育背景</h2>
                <div class="timeline-item">
                    <h3>学位名称</h3>
                    <p class="timeline-date">2019年9月 - 2023年6月</p>
                    <p><strong>学校名称</strong>, 城市, 国家</p>
                    <p>专业: 你的专业</p>
                    <p>GPA: X.X/4.0</p>
                    <p>相关课程: 课程一, 课程二, 课程三</p>
                </div>
                <div class="timeline-item">
                    <h3>学位名称</h3>
                    <p class="timeline-date">2016年9月 - 2019年6月</p>
                    <p><strong>学校名称</strong>, 城市, 国家</p>
                    <p>专业: 你的专业</p>
                </div>
            </section>
            
            <!-- 研究经历 -->
            <section id="research" class="section">
                <h2>研究经历</h2>
                <div class="timeline-item">
                    <h3>研究职位/项目名称</h3>
                    <p class="timeline-date">2022年3月 - 2023年5月</p>
                    <p><strong>实验室/学校名称</strong>, 导师: 导师姓名</p>
                    <ul>
                        <li>研究内容和成果一</li>
                        <li>研究内容和成果二</li>
                        <li>使用的方法和技术</li>
                    </ul>
                </div>
                <div class="timeline-item">
                    <h3>研究职位/项目名称</h3>
                    <p class="timeline-date">2021年6月 - 2022年2月</p>
                    <p><strong>实验室/学校名称</strong>, 导师: 导师姓名</p>
                    <ul>
                        <li>研究内容和成果一</li>
                        <li>研究内容和成果二</li>
                    </ul>
                </div>
            </section>
            
            <!-- 学术成果 -->
            <section id="publications" class="section">
                <h2>学术成果</h2>
                <div class="publication-list">
                    <div class="timeline-item">
                        <h3>论文标题</h3>
                        <p class="timeline-date">2023年</p>
                        <p><strong>作者</strong>, 会议/期刊名称, 卷(期), 页码</p>
                        <p><a href="#">链接到论文</a> | <a href="#">PDF</a> | <a href="#">代码</a></p>
                    </div>
                    <div class="timeline-item">
                        <h3>论文标题</h3>
                        <p class="timeline-date">2022年</p>
                        <p><strong>作者</strong>, 会议/期刊名称, 卷(期), 页码</p>
                        <p><a href="#">链接到论文</a> | <a href="#">PDF</a></p>
                    </div>
                </div>
            </section>
            
            <!-- 项目作品 -->
            <section id="projects" class="section">
                <h2>项目作品</h2>
                <div class="projects-grid">
                    <div class="project-card">
                        <h3>项目名称</h3>
                        <p>项目描述，包括使用的技术、实现的功能等。</p>
                        <p><strong>技术栈:</strong> 技术一, 技术二, 技术三</p>
                        <p><a href="#">代码链接</a> | <a href="#">演示链接</a></p>
                    </div>
                    <div class="project-card">
                        <h3>项目名称</h3>
                        <p>项目描述，包括使用的技术、实现的功能等。</p>
                        <p><strong>技术栈:</strong> 技术一, 技术二, 技术三</p>
                        <p><a href="#">代码链接</a></p>
                    </div>
                    <div class="project-card">
                        <h3>项目名称</h3>
                        <p>项目描述，包括使用的技术、实现的功能等。</p>
                        <p><strong>技术栈:</strong> 技术一, 技术二, 技术三</p>
                        <p><a href="#">代码链接</a> | <a href="#">文档</a></p>
                    </div>
                </div>
            </section>
            
            <!-- 实习经历 -->
            <section id="internship" class="section">
                <h2>实习经历</h2>
                <div class="timeline-item">
                    <h3>职位名称</h3>
                    <p class="timeline-date">2022年6月 - 2022年9月</p>
                    <p><strong>公司名称</strong>, 城市, 国家</p>
                    <ul>
                        <li>工作职责和成就一</li>
                        <li>工作职责和成就二</li>
                        <li>使用的技术栈和工具</li>
                    </ul>
                </div>
                <div class="timeline-item">
                    <h3>职位名称</h3>
                    <p class="timeline-date">2021年7月 - 2021年8月</p>
                    <p><strong>公司名称</strong>, 城市, 国家</p>
                    <ul>
                        <li>工作职责和成就一</li>
                        <li>工作职责和成就二</li>
                    </ul>
                </div>
            </section>
        </main>
    </div>

    <script>
        // 平滑滚动导航
        document.querySelectorAll('.nav-link').forEach(link => {
            link.addEventListener('click', function(e) {
                e.preventDefault();
                const targetId = this.getAttribute('href');
                const targetSection = document.querySelector(targetId);
                window.scrollTo({
                    top: targetSection.offsetTop - 80,
                    behavior: 'smooth'
                });
            });
        });
        
        // 根据滚动位置高亮导航链接
        window.addEventListener('scroll', function() {
            const sections = document.querySelectorAll('.section');
            const navLinks = document.querySelectorAll('.nav-link');
            
            let current = '';
            sections.forEach(section => {
                const sectionTop = section.offsetTop;
                const sectionHeight = section.clientHeight;
                if (pageYOffset >= sectionTop - 100) {
                    current = section.getAttribute('id');
                }
            });
            
            navLinks.forEach(link => {
                link.classList.remove('active');
                if (link.getAttribute('href').substring(1) === current) {
                    link.classList.add('active');
                }
            });
        });
    </script>
</body>
</html>
