<!DOCTYPE html>
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
            background-color: #f8f9fa;
        }

        .container {
            display: flex;
            min-height: 100vh;
        }

        /* 左侧边栏样式 */
        .sidebar {
            flex: 0 0 320px;
            background: linear-gradient(135deg, #a7c5eb 0%, #7fb0d3 100%);
            color: white;
            padding: 2rem;
            position: fixed;
            width: 320px;
            height: 100vh;
            overflow-y: auto;
        }

        .profile-header {
            text-align: center;
            margin-bottom: 1.5rem;
        }

        .profile-header h1 {
            font-size: 1.8rem;
            margin-bottom: 0.5rem;
        }

        .profile-header .title {
            font-size: 1rem;
            opacity: 0.9;
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

        .section-block {
            margin: 1.5rem 0;
        }

        .section-block h3 {
            margin-bottom: 0.8rem;
            font-size: 1.1rem;
            border-bottom: 1px solid rgba(255,255,255,0.3);
            padding-bottom: 0.3rem;
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

        .language-item {
            display: flex;
            justify-content: space-between;
            margin-bottom: 0.5rem;
            font-size: 0.9rem;
        }

        .social-link {
            color: white;
            text-decoration: none;
            display: flex;
            align-items: center;
            margin-bottom: 0.5rem;
        }

        .social-link:hover {
            text-decoration: underline;
        }

        /* 右侧主内容区样式 */
        .main-content {
            flex: 1;
            margin-left: 320px;
            padding: 2rem 3rem;
            background: white;
        }

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

        .nav-link:hover, .nav-link.active {
            background: #3498db;
            color: white;
        }

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
            font-weight: 500;
        }

        .responsibility-list {
            margin-top: 0.8rem;
            padding-left: 1.2rem;
        }

        .responsibility-list li {
            margin-bottom: 0.5rem;
        }

        .honors-list {
            margin-top: 1rem;
        }

        .honor-item {
            margin-bottom: 0.8rem;
            padding-bottom: 0.8rem;
            border-bottom: 1px solid #eee;
        }

        .honor-item:last-child {
            border-bottom: none;
        }

        .publication-item {
            margin-bottom: 2rem;
            padding: 1.5rem;
            background: #f8f9fa;
            border-radius: 8px;
        }

        .publication-link {
            display: inline-block;
            margin-top: 0.5rem;
            color: #3498db;
            text-decoration: none;
            font-weight: 500;
        }

        .publication-link:hover {
            text-decoration: underline;
        }

        .blog-posts {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 1.5rem;
            margin-top: 1.5rem;
        }

        .blog-post {
            background: #f8f9fa;
            padding: 1.5rem;
            border-radius: 8px;
            border-left: 4px solid #3498db;
            transition: transform 0.3s ease;
        }

        .blog-post:hover {
            transform: translateY(-5px);
        }

        .blog-post h3 {
            margin-bottom: 0.8rem;
            color: #2c3e50;
        }

        .blog-meta {
            color: #7f8c8d;
            font-size: 0.9rem;
            margin-bottom: 0.8rem;
        }

        .blog-link {
            display: inline-block;
            margin-top: 0.8rem;
            color: #3498db;
            text-decoration: none;
            font-weight: 500;
        }

        .blog-link:hover {
            text-decoration: underline;
        }

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
            
            .blog-posts {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- 左侧边栏 - 个人信息 -->
        <aside class="sidebar">
            <div class="profile-header">
                <h1>何奕峰</h1>
                <p class="title">香港中文大学 硕士 | 对外英语教学</p>
                <p class="title">中共预备党员 | MBTI: ISTJ</p>
            </div>
            
            <div class="contact-info">
                <div class="contact-item">
                    <i class="fas fa-envelope"></i>
                    <span>1155249818@link.cuhk.edu.hk</span>
                </div>
                <div class="contact-item">
                    <i class="fas fa-map-marker-alt"></i>
                    <span>上海 / 深圳 / 香港</span>
                </div>
                <div class="contact-item">
                    <i class="fab fa-linkedin"></i>
                    <a href="https://www.linkedin.com/in/yifeng-he-863a57353/" class="social-link" target="_blank">LinkedIn</a>
                </div>
            </div>
            
            <div class="section-block">
                <h3>关于我</h3>
                <p>对外英语教学专业研究生，具备人力资源、教育发展和国际组织等多领域实践经验，致力于跨文化交流与教育创新。</p>
            </div>
            
            <div class="section-block">
                <h3>语言能力</h3>
                <div class="language-item">
                    <span>英文</span>
                    <span>雅思7.5 | 专八优秀</span>
                </div>
                <div class="language-item">
                    <span>中文</span>
                    <span>普通话二甲</span>
                </div>
            </div>
            
            <div class="section-block">
                <h3>专业技能</h3>
                <div class="skill-tags">
                    <span class="skill-tag">人才Mapping</span>
                    <span class="skill-tag">校园招聘</span>
                    <span class="skill-tag">活动策划</span>
                    <span class="skill-tag">项目管理</span>
                    <span class="skill-tag">数据分析</span>
                </div>
            </div>
            
            <div class="section-block">
                <h3>软件技能</h3>
                <div class="skill-tags">
                    <span class="skill-tag">Office</span>
                    <span class="skill-tag">秀米</span>
                    <span class="skill-tag">可画</span>
                    <span class="skill-tag">剪映</span>
                    <span class="skill-tag">Illustrator</span>
                    <span class="skill-tag">Publisher</span>
                </div>
            </div>
        </aside>
        
        <!-- 右侧主内容区 -->
        <main class="main-content">
            <!-- 导航栏 -->
            <nav class="navbar">
                <div class="nav-links">
                    <a href="#education" class="nav-link">教育背景</a>
                    <a href="#internship" class="nav-link">实习经历</a>
                    <a href="#campus" class="nav-link">校园经历</a>
                    <a href="#honors" class="nav-link">荣誉奖项</a>
                    <a href="#publications" class="nav-link">论文发表</a>
                    <a href="#blogs" class="nav-link">推文作品</a>
                    <a href="#evaluation" class="nav-link">自我评价</a>
                </div>
            </nav>
            
            <!-- 教育背景 -->
            <section id="education" class="section">
                <h2>教育背景</h2>
                <div class="timeline-item">
                    <h3>香港中文大学</h3>
                    <p class="timeline-date">2025.09 - 2026.11 (预期)</p>
                    <p><strong>硕士学位 - 对外英语教学</strong></p>
                </div>
                <div class="timeline-item">
                    <h3>南京大学</h3>
                    <p class="timeline-date">2021.09 - 2025.06</p>
                    <p><strong>学士学位 - 英语专业</strong></p>
                </div>
            </section>
            
            <!-- 实习经历 -->
            <section id="internship" class="section">
                <h2>实习经历</h2>
                
                <div class="timeline-item">
                    <h3>小红书科技有限公司 - 校招组实习生</h3>
                    <p class="timeline-date">2025.06 - 至今 | 上海 & 深圳</p>
                    <ul class="responsibility-list">
                        <li><strong>工程侧 Mapping</strong>：采用"校队+个人"双路径，摸排近三年国际级、国家级、企业级竞赛逾50场，锁定10所目标院校校队；通过竞赛、实习等维度 mapping 200余人</li>
                        <li><strong>算法侧 Mapping</strong>：独立完成10所目标高校技术类专业和50余个重点实验室/课题组人才mapping，累计mapping应届学生980余人，为人才库扩充近300份有效简历</li>
                        <li><strong>顶会渠道开源</strong>：独立 mapping 9个顶会，累计 mapping 3200余人，已邮件触达1300余人，建联380人</li>
                        <li><strong>高校渠道开源</strong>：根据算法、运营、产品等职位人才计划，完成20余个目标高校和30余个院系的定向宣传</li>
                        <li><strong>面试流程管理</strong>：负责工程侧候选人集中面试安排，完成超200位候选人面试邀约与进度跟进</li>
                        <li><strong>校园大使运营</strong>：负责泛技术类校园大使简历筛选与面试选拔，跟进30位校园大使后续工作情况</li>
                    </ul>
                </div>
                
                <div class="timeline-item">
                    <h3>安永华明会计师事务所 - 社招组实习生</h3>
                    <p class="timeline-date">2025.02 - 2025.05 | 上海</p>
                    <ul class="responsibility-list">
                        <li><strong>人才招募</strong>：熟练运用猎聘、前程无忧等招聘渠道，独立完成气候变化与可持续发展咨询、（非）金融审计、网络安全、工程造价等多个岗位人才寻聘，完成300余位候选人触达，超30位候选人成功入职</li>
                        <li><strong>面试跟进</strong>：完成70余场次面试材料准备、候选人联络及面试情况跟进，面试准时率超95%；及时更新面试信息，为通过面试候选人撰写薪资提案，保证候选人offer顺利发放</li>
                    </ul>
                </div>
                
                <div class="timeline-item">
                    <h3>国际救助儿童会 - 0-6岁儿童早期发展项目实习生</h3>
                    <p class="timeline-date">2024.06 - 2024.12 | 上海</p>
                    <ul class="responsibility-list">
                        <li><strong>活动规划与执行</strong>：全程参与乐高亲子活动、项目总结会等活动筹备，协助举办常规项目点家长讲座、亲子活动超20场，统计并更新200余名参与者信息</li>
                        <li><strong>物料设计与审核</strong>：根据机构设计风格要求，独立完成活动折页、海报、推文设计与制作，与承接方沟通协调完成活动易拉宝和主题背景板等宣传品进度跟进、审校和优化</li>
                        <li><strong>财务与行政管理</strong>：处理费用报销、物资采购及活动文档归档，与各协办方沟通确保项目高效执行</li>
                    </ul>
                </div>
            </section>
            
            <!-- 校园经历 -->
            <section id="campus" class="section">
                <h2>校园经历</h2>
                
                <div class="timeline-item">
                    <h3>南播玩工作室 - 总监助理</h3>
                    <p class="timeline-date">2023.06 - 2024.06 | 江苏南京</p>
                    <ul class="responsibility-list">
                        <li><strong>会议统筹</strong>：组织安排50余场联席会、主任办公会等会议，及时发布会议记录，确保会议决议有效落实</li>
                        <li><strong>企业文化</strong>：定期进行企业文化培训，传达郑钢基金会动态；累计组织9场部门间团建，提升工作室凝聚力</li>
                        <li><strong>绩效管理</strong>：负责跟进各部门绩效标准制定，核查120余人月度考核结果，并表彰优秀部员</li>
                        <li><strong>培训开发</strong>：牵头完成月度业务培训课程10余场，提升员工对核心业务技能掌握程度，扩充核心业务团队</li>
                    </ul>
                </div>
                
                <div class="timeline-item">
                    <h3>南京大学学生模拟联合国协会 - 副会长 & 宣传总监</h3>
                    <p class="timeline-date">2022.09 - 2024.08 | 江苏南京</p>
                    <ul class="responsibility-list">
                        <li><strong>协会运营与管理</strong>：全面负责协会日常运营，完成15项社团活动申报与总结，确保活动顺利开展</li>
                        <li><strong>品牌活动筹办</strong>：筹划并落地社团品牌活动，活动受众累计覆盖全国80余所学校、超500人次</li>
                        <li><strong>宣传推广</strong>：负责2024年南京大学模拟联合国大会宣传工作，完成30篇推文制作、7件物料设计、闭幕式视频剪辑、人物专访等，针对30余个目标协会进行建联与定向宣传，推文总浏览量超24000</li>
                    </ul>
                </div>
                
                <div class="timeline-item">
                    <h3>其他学生工作</h3>
                    <p class="timeline-date">2021 - 2024 | 南京大学</p>
                    <ul class="responsibility-list">
                        <li><strong>外院实践创新部部长</strong> - 组织策划学院实践创新活动</li>
                        <li><strong>英语 A 班班长</strong> - 负责班级日常管理与活动组织</li>
                        <li><strong>模联协会临时团支部团支书</strong> - 领导团支部建设与活动</li>
                        <li><strong>国际组织发展协会部长</strong> - 推动国际组织相关活动发展</li>
                    </ul>
                </div>
            </section>
            
            <!-- 荣誉奖项 -->
            <section id="honors" class="section">
                <h2>荣誉奖项</h2>
                <div class="honors-list">
                    <div class="honor-item">
                        <h3>人民奖学金</h3>
                        <p>南京大学校级奖学金，表彰在学习和综合素质方面表现优秀的学生</p>
                    </div>
                    <div class="honor-item">
                        <h3>郑钢菁英奖学金</h3>
                        <p>专项精英奖学金，奖励在专业领域有突出表现的学生</p>
                    </div>
                    <div class="honor-item">
                        <h3>国际组织人才奖学金</h3>
                        <p>国际组织发展专项奖学金，培养具有国际视野的人才</p>
                    </div>
                    <div class="honor-item">
                        <h3>徐琛-江满奖学金</h3>
                        <p>社会捐赠奖学金，奖励品学兼优的学生</p>
                    </div>
                    <div class="honor-item">
                        <h3>优秀学生社团骨干</h3>
                        <p>表彰在学生社团工作中表现突出的骨干成员</p>
                    </div>
                </div>
            </section>
            
            <!-- 论文发表 -->
            <section id="publications" class="section">
                <h2>论文发表</h2>
                <div class="publication-item">
                    <p><strong>He, Y.,</strong> Chen, L., Wang, M., & Liu, X. (2024). 英语专业学生跨文化交际能力培养路径研究. <em>现代教育研究</em>, 12(3), 45-52. http://www.isciencegroup.com/cn/articleinfo/10440071</p>
                    <a href="http://www.isciencegroup.com/cn/articleinfo/10440071" class="publication-link" target="_blank">查看论文全文 →</a>
                </div>
            </section>
            
            <!-- 推文作品 -->
            <section id="blogs" class="section">
                <h2>推文作品</h2>
                <div class="blog-posts">
                    <div class="blog-post">
                        <h3>模联大会回顾 | 青年外交官的成长之旅</h3>
                        <div class="blog-meta">发布于 2024年5月 | 南播玩工作室</div>
                        <a href="https://mp.weixin.qq.com/s/jmioeHj3xxTB4y6DtF_vva" class="blog-link" target="_blank">阅读全文 →</a>
                    </div>
                    <div class="blog-post">
                        <h3>国际组织实习经验分享</h3>
                        <div class="blog-meta">发布于 2024年3月 | 南播玩工作室</div>
                        <a href="https://mp.weixin.qq.com/s/jPyS_MG5eMgTgrMfJtkg0Q" class="blog-link" target="_blank">阅读全文 →</a>
                    </div>
                    <div class="blog-post">
                        <h3>校园招聘新趋势 | 人才Mapping实战解析</h3>
                        <div class="blog-meta">发布于 2024年8月 | 南播玩工作室</div>
                        <a href="https://mp.weixin.qq.com/s/sKZze8Bny8qJrV7FX8w9oA" class="blog-link" target="_blank">阅读全文 →</a>
                    </div>
                </div>
            </section>
            
            <!-- 自我评价 -->
            <section id="evaluation" class="section">
                <h2>自我评价</h2>
                <div class="self-evaluation">
                    <div class="evaluation-point">
                        <h4>人力资源专业能力</h4>
                        <p>具备招聘的实习经历与创业公司的多模块工作经验，具备人才Mapping与活动筹办等专业能力，熟悉校园招聘全流程。</p>
                    </div>
                    <div class="evaluation-point">
                        <h4>多领域的工作经验</h4>
                        <p>拥有互联网、审计、咨询、国际组织等多领域实习经历，具备跨行业思维与实操经验，能够快速适应不同工作环境。</p>
                    </div>
                    <div class="evaluation-point">
                        <h4>相匹配的性格态度</h4>
                        <p>能够进行高效沟通，也能细致入微地完成各项工作，具备快速的学习能力与负责的工作态度，善于团队协作与项目管理。</p>
                    </div>
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
