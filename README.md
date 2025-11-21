# HyphenHe.github.io
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>我的GitHub主页</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <!-- 导航栏 -->
    <nav class="navbar">
        <div class="nav-container">
            <div class="nav-links">
                <a href="#" class="nav-link active" data-tab="home">首页</a>
                <a href="#" class="nav-link" data-tab="publications">学术成果</a>
                <a href="#" class="nav-link" data-tab="internship">实习经历</a>
                <a href="#" class="nav-link" data-tab="education">教育背景</a>
                <a href="#" class="nav-link" data-tab="projects">项目作品</a>
            </div>
        </div>
    </nav>

    <!-- 主要内容区 -->
    <main class="main-container">
        <!-- 左侧边栏 - 个人信息 -->
        <aside class="sidebar">
            <div class="profile-card">
                <div class="profile-image">
                    <img src="https://via.placeholder.com/200x200/4A90E2/ffffff?text=Your+Photo" alt="个人照片" id="profile-pic">
                </div>
                <div class="profile-info">
                    <h1 id="username">你的名字</h1>
                    <p class="title" id="job-title">职位/专业</p>
                    <p class="bio" id="user-bio">这里是一段简短的自我介绍，描述你的技术栈、兴趣方向和个人特点。</p>
                    
                    <div class="contact-info">
                        <div class="contact-item">
                            <span>📧</span>
                            <span id="email">your.email@example.com</span>
                        </div>
                        <div class="contact-item">
                            <span>📍</span>
                            <span id="location">所在城市</span>
                        </div>
                    </div>

                    <div class="skills">
                        <h3>技术技能</h3>
                        <div class="skill-tags">
                            <span class="skill-tag">HTML/CSS</span>
                            <span class="skill-tag">JavaScript</span>
                            <span class="skill-tag">Python</span>
                            <span class="skill-tag">Git</span>
                        </div>
                    </div>

                    <div class="social-links">
                        <a href="#" class="social-link">GitHub</a>
                        <a href="#" class="social-link">LinkedIn</a>
                        <a href="#" class="social-link">博客</a>
                    </div>
                </div>
            </div>
        </aside>

        <!-- 右侧内容区 -->
        <section class="content">
            <!-- 首页内容 -->
            <div class="tab-content active" id="home-content">
                <h2>欢迎访问我的主页</h2>
                <div class="welcome-section">
                    <p>这里是我的个人空间，展示我的学习历程、项目经验和成长轨迹。</p>
                    
                    <div class="highlights">
                        <div class="highlight-card">
                            <h3>🎯 当前关注</h3>
                            <p>正在学习的前沿技术或研究的领域</p>
                        </div>
                        <div class="highlight-card">
                            <h3>🚀 最新动态</h3>
                            <p>最近完成的项目或取得的成就</p>
                        </div>
                    </div>
                </div>
            </div>

            <!-- 学术成果 -->
            <div class="tab-content" id="publications-content">
                <h2>学术成果</h2>
                <div class="publication-list">
                    <div class="publication-item">
                        <h3>论文标题一</h3>
                        <p class="publication-meta">期刊/会议名称, 2024</p>
                        <p>论文摘要或描述...</p>
                        <a href="#" class="publication-link">查看详情</a>
                    </div>
                    <div class="publication-item">
                        <h3>论文标题二</h3>
                        <p class="publication-meta">期刊/会议名称, 2023</p>
                        <p>论文摘要或描述...</p>
                        <a href="#" class="publication-link">查看详情</a>
                    </div>
                </div>
            </div>

            <!-- 实习经历 -->
            <div class="tab-content" id="internship-content">
                <h2>实习经历</h2>
                <div class="timeline">
                    <div class="timeline-item">
                        <h3>公司名称</h3>
                        <p class="timeline-meta">职位 | 2024年1月 - 2024年6月</p>
                        <ul>
                            <li>工作职责和成就一</li>
                            <li>工作职责和成就二</li>
                            <li>使用的技术栈和工具</li>
                        </ul>
                    </div>
                    <div class="timeline-item">
                        <h3>公司名称</h3>
                        <p class="timeline-meta">职位 | 2023年6月 - 2023年9月</p>
                        <ul>
                            <li>工作职责和成就一</li>
                            <li>工作职责和成就二</li>
                        </ul>
                    </div>
                </div>
            </div>

            <!-- 教育背景 -->
            <div class="tab-content" id="education-content">
                <h2>教育背景</h2>
                <div class="education-list">
                    <div class="education-item">
                        <h3>大学名称</h3>
                        <p class="education-meta">学位 | 专业 | 2022年 - 2026年</p>
                        <p>主修课程：课程一，课程二，课程三</p>
                        <p>GPA: X.X/4.0</p>
                    </div>
                    <div class="education-item">
                        <h3>高中名称</h3>
                        <p class="education-meta">毕业时间 | 2019年 - 2022年</p>
                    </div>
                </div>
            </div>

            <!-- 项目作品 -->
            <div class="tab-content" id="projects-content">
                <h2>项目作品</h2>
                <div class="projects-grid">
                    <div class="project-card">
                        <h3>项目名称一</h3>
                        <p>项目描述和技术栈...</p>
                        <div class="project-links">
                            <a href="#" class="project-link">代码</a>
                            <a href="#" class="project-link">演示</a>
                        </div>
                    </div>
                    <div class="project-card">
                        <h3>项目名称二</h3>
                        <p>项目描述和技术栈...</p>
                        <div class="project-links">
                            <a href="#" class="project-link">代码</a>
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </main>

    <script src="script.js"></script>
</body>
</html>
