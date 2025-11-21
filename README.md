<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
    <title>何奕峰 - 个人主页</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" />
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
            background-color: white;
            min-height: 100vh;
            padding: 2rem;
            max-width: 900px;
            margin: 0 auto;
        }
        header {
            text-align: center;
            margin-bottom: 2rem;
        }
        h1 {
            font-size: 2.2rem;
            color: #2c3e50;
            margin-bottom: 0.5rem;
        }
        .subtitle {
            color: #7f8c8d;
            margin-bottom: 1.5rem;
        }
        .social-links {
            display: flex;
            justify-content: center;
            gap: 1.2rem;
            margin-bottom: 2rem;
            flex-wrap: wrap;
        }
        .social-link {
            color: #3498db;
            text-decoration: none;
            font-weight: 500;
            display: flex;
            align-items: center;
            gap: 0.4rem;
        }
        .social-link:hover {
            text-decoration: underline;
        }
        .intro {
            background: #f8f9fa;
            padding: 1.5rem;
            border-radius: 8px;
            margin-bottom: 2rem;
            line-height: 1.7;
        }
        .intro p {
            margin-bottom: 0.8rem;
        }
        .nav-links {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 1rem;
        }
        .nav-item {
            padding: 1rem;
            background: #f8f9fa;
            text-align: center;
            border-radius: 8px;
            text-decoration: none;
            color: #2c3e50;
            font-weight: 500;
            transition: transform 0.2s;
        }
        .nav-item:hover {
            transform: translateY(-3px);
            background: #eef2f7;
        }
        .lang-switch {
            text-align: center;
            margin-top: 2rem;
            padding-top: 1.5rem;
            border-top: 1px solid #eee;
        }
        .lang-link {
            color: #9b59b6;
            text-decoration: none;
            font-size: 0.95rem;
        }
        .lang-link:hover {
            text-decoration: underline;
        }
        @media (max-width: 600px) {
            body {
                padding: 1rem;
            }
            .social-links {
                gap: 0.8rem;
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>何奕峰</h1>
        <div class="subtitle">人力资源 | 招聘 | 跨领域实践者</div>

        <div class="social-links">
            <a href="mailto:yifenghe01@gmail.com" class="social-link">
                <i class="fas fa-envelope"></i> yifenghe01@gmail.com
            </a>
            <a href="https://www.linkedin.com/in/yifeng-he-7b0a0b23a/" target="_blank" class="social-link">
                <i class="fab fa-linkedin"></i> LinkedIn
            </a>
            <a href="https://github.com/HyphenHe" target="_blank" class="social-link">
                <i class="fab fa-github"></i> GitHub
            </a>
        </div>

        <div class="intro">
            <p>你好！我是何奕峰，目前就读于香港中文大学，预计于2026年11月毕业。我此前分别在安永EY和小红书做招聘实习生，目前正在看人力资源岗位的实习/工作机会~</p>
            <p><strong>一些自我评价：</strong></p>
            <ul style="padding-left: 1.2rem; margin-top: 0.5rem;">
                <li><strong>人力资源专业能力</strong>：具备招聘的实习经历与创业公司的多模块工作经验，具备人才Mapping与活动筹办等能力</li>
                <li><strong>多领域的工作经验</strong>：曾进行互联网、审计、咨询、国际组织的实习，具备多领域、跨行业的思维与实操经验</li>
                <li><strong>相匹配的性格态度</strong>：能够进行高效沟通，也能细致入微地完成各项工作，具备快速的学习能力与负责的工作态度</li>
            </ul>
        </div>
    </header>

    <div class="nav-links">
        <a href="education.html" class="nav-item">教育背景</a>
        <a href="campus.html" class="nav-item">校园与媒体</a>
    </div>

    <div class="lang-switch">
        <a href="en.html" class="lang-link">→ English Version (Coming Soon)</a>
    </div>
</body>
</html>
