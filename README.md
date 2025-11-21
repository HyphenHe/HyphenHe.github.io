<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>何奕峰 - 个人主页</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
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
            background: linear-gradient(135deg, #a7c5eb 0%, #f8cdda 100%);
            min-height: 100vh;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 2rem;
        }

        .main-content {
            background: rgba(255, 255, 255, 0.95);
            border-radius: 15px;
            padding: 3rem;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            text-align: center;
        }

        .profile-header {
            margin-bottom: 2rem;
        }

        .profile-header h1 {
            font-size: 3rem;
            color: #2c3e50;
            margin-bottom: 1rem;
        }

        .personal-info {
            margin: 1.5rem 0;
            font-size: 1.1rem;
            color: #555;
        }

        .contact-icons {
            display: flex;
            justify-content: center;
            gap: 2rem;
            margin: 2rem 0;
        }

        .contact-icon {
            display: flex;
            flex-direction: column;
            align-items: center;
            text-decoration: none;
            color: #2c3e50;
            transition: transform 0.3s ease;
        }

        .contact-icon:hover {
            transform: translateY(-5px);
        }

        .contact-icon i {
            font-size: 2rem;
            margin-bottom: 0.5rem;
            background: linear-gradient(135deg, #a7c5eb, #f8cdda);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .nav-section {
            margin-top: 3rem;
        }

        .nav-links {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1.5rem;
            margin-top: 1.5rem;
        }

        .nav-link {
            background: linear-gradient(135deg, #a7c5eb 0%, #7fb0d3 100%);
            color: white;
            padding: 1.5rem;
            border-radius: 10px;
            text-decoration: none;
            font-weight: 500;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
        }

        .nav-link:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 20px rgba(0, 0, 0, 0.15);
        }

        .nav-link i {
            font-size: 1.5rem;
            margin-bottom: 0.5rem;
        }

        @media (max-width: 768px) {
            .main-content {
                padding: 2rem;
            }
            
            .profile-header h1 {
                font-size: 2rem;
            }
            
            .contact-icons {
                flex-direction: column;
                gap: 1rem;
            }
            
            .nav-links {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="main-content">
            <div class="profile-header">
                <h1>何奕峰</h1>
                <p class="title">香港中文大学 硕士 | 对外英语教学</p>
            </div>
            
            <div class="personal-info">
                <p>中共预备党员 | MBTI: ISTJ</p>
                <p>工作城市：上海 / 深圳 / 香港</p>
            </div>
            
            <div class="contact-icons">
                <a href="mailto:1155249818@link.cuhk.edu.hk" class="contact-icon">
                    <i class="fas fa-envelope"></i>
                    <span>邮箱</span>
                </a>
                <a href="https://www.linkedin.com/in/yifeng-he-863a57353/" class="contact-icon" target="_blank">
                    <i class="fab fa-linkedin"></i>
                    <span>LinkedIn</span>
                </a>
                <a href="index.html" class="contact-icon">
                    <i class="fas fa-home"></i>
                    <span>主页</span>
                </a>
            </div>
            
            <div class="nav-section">
                <h2>导航菜单</h2>
                <div class="nav-links">
                    <a href="education.html" class="nav-link" target="_blank">
                        <i class="fas fa-graduation-cap"></i>
                        <div>教育背景</div>
                    </a>
                    <a href="internship.html" class="nav-link" target="_blank">
                        <i class="fas fa-briefcase"></i>
                        <div>实习经历</div>
                    </a>
                    <a href="campus.html" class="nav-link" target="_blank">
                        <i class="fas fa-users"></i>
                        <div>校园经历</div>
                    </a>
                    <a href="honors.html" class="nav-link" target="_blank">
                        <i class="fas fa-trophy"></i>
                        <div>荣誉奖项</div>
                    </a>
                    <a href="publications.html" class="nav-link" target="_blank">
                        <i class="fas fa-book"></i>
                        <div>论文发表</div>
                    </a>
                    <a href="blogs.html" class="nav-link" target="_blank">
                        <i class="fas fa-pen"></i>
                        <div>推文作品</div>
                    </a>
                    <a href="evaluation.html" class="nav-link" target="_blank">
                        <i class="fas fa-user"></i>
                        <div>自我评价</div>
                    </a>
                </div>
            </div>
        </div>
    </div>
</body>
</html>
