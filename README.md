<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hyun's GitHub Profile</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            padding: 20px;
        }
        
        .container {
            max-width: 1000px;
            margin: 0 auto;
            background: white;
            border-radius: 20px;
            box-shadow: 0 20px 40px rgba(0,0,0,0.1);
            overflow: hidden;
        }
        
        .header {
            background: linear-gradient(135deg, #24292e 0%, #0366d6 100%);
            color: white;
            padding: 60px 40px;
            text-align: center;
            position: relative;
        }
        

        
        .header h1 {
            font-size: 3.5rem;
            margin-bottom: 15px;
            animation: fadeIn 1s ease-in;
        }
        
        .header p {
            font-size: 1.3rem;
            opacity: 0.9;
            animation: fadeIn 1.5s ease-in;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .content {
            padding: 40px;
        }
        
        .section {
            margin-bottom: 50px;
            padding: 30px;
            border-radius: 15px;
            background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
            box-shadow: 0 5px 15px rgba(0,0,0,0.08);
            transition: transform 0.3s ease;
        }
        
        .section:hover {
            transform: translateY(-5px);
        }
        
        .section-title {
            font-size: 1.8rem;
            font-weight: bold;
            color: #24292e;
            margin-bottom: 25px;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .tech-stack {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            justify-content: center;
        }
        
        .tech-badge {
            background: linear-gradient(135deg, #28a745, #20c997);
            color: white;
            padding: 12px 20px;
            border-radius: 25px;
            font-size: 1rem;
            font-weight: 600;
            text-decoration: none;
            transition: all 0.3s ease;
            box-shadow: 0 3px 10px rgba(40, 167, 69, 0.3);
        }
        
        .tech-badge:hover {
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(40, 167, 69, 0.4);
        }
        
        .java { background: linear-gradient(135deg, #007396, #005a7a); }
        .spring { background: linear-gradient(135deg, #6DB33F, #5a9e35); }
        .javascript { background: linear-gradient(135deg, #F7DF1E, #d4c01e); color: black; }
        .html { background: linear-gradient(135deg, #E34F26, #c73e1d); }
        .css { background: linear-gradient(135deg, #1572B6, #0f5a94); }
        .oracle { background: linear-gradient(135deg, #F80000, #d40000); }
        .mysql { background: linear-gradient(135deg, #4479A1, #336688); }
        
        .contact-section {
            text-align: center;
        }
        
        .contact-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            flex-wrap: wrap;
        }
        
        .contact-btn {
            background: linear-gradient(135deg, #6f42c1, #e83e8c);
            color: white;
            padding: 15px 30px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
            box-shadow: 0 5px 15px rgba(111, 66, 193, 0.3);
        }
        
        .contact-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(111, 66, 193, 0.4);
        }
        
        .gmail { background: linear-gradient(135deg, #D14836, #b73e2e); }
        .naver { background: linear-gradient(135deg, #03C75A, #02a049); }
        
        .stats-section {
            text-align: center;
        }
        
        .stats-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-top: 30px;
        }
        
        .stat-card {
            background: white;
            padding: 25px;
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            transition: transform 0.3s ease;
        }
        
        .stat-card:hover {
            transform: scale(1.05);
        }
        
        .stat-placeholder {
            width: 100%;
            height: 200px;
            background: linear-gradient(135deg, #24292e, #0366d6);
            border-radius: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: bold;
            margin-bottom: 15px;
        }
        
        .baekjoon-placeholder {
            background: linear-gradient(135deg, #0076C0, #005a94);
        }
        
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
        }
        
        .stat-card {
            background: white;
            padding: 25px;
            border-radius: 15px;
            text-align: center;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            transition: transform 0.3s ease;
        }
        
        .stat-card:hover {
            transform: translateY(-3px);
        }
        
        .stat-number {
            font-size: 2.5rem;
            font-weight: bold;
            color: #0366d6;
            margin-bottom: 10px;
        }
        
        .activity-graph {
            background: #f6f8fa;
            padding: 30px;
            border-radius: 15px;
            text-align: center;
        }
        
        .graph-placeholder {
            height: 120px;
            background: linear-gradient(90deg, #ebedf0 0%, #c6e48b 25%, #7bc96f 50%, #239a3b 75%, #196127 100%);
            border-radius: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: bold;
            font-size: 1.2rem;
            text-shadow: 1px 1px 2px rgba(0,0,0,0.3);
        }
        
        .footer {
            background: #24292e;
            color: white;
            text-align: center;
            padding: 30px;
            margin-top: 40px;
        }
        
        .emoji {
            font-size: 1.5rem;
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- 헤더 섹션 -->
        <div class="header">
            <h1>🌊 Hyun's Profile</h1>
            <p>꿈을 향해 나아가는 개발자 최현섭입니다.</p>

        </div>
        
        <div class="content">
            <!-- 기술 스택 섹션 -->
            <div class="section">
                <div class="section-title">
                    <span class="emoji">🔧</span>
                    Tech Stack
                </div>
                <div class="tech-stack">
                    <span class="tech-badge java">Java</span>
                    <span class="tech-badge spring">Spring</span>
                    <span class="tech-badge spring">Spring Boot</span>
                    <span class="tech-badge javascript">JavaScript</span>
                    <span class="tech-badge html">HTML5</span>
                    <span class="tech-badge css">CSS3</span>
                    <span class="tech-badge oracle">Oracle</span>
                    <span class="tech-badge mysql">MySQL</span>
                </div>
            </div>
            
            <!-- GitHub 통계 섹션 -->
            <div class="section">
                <div class="section-title">
                    <span class="emoji">📊</span>
                    GitHub Statistics
                </div>
                <div class="stats-grid">
                    <div class="stat-card">
                        <div class="stat-number">150+</div>
                        <div>Total Commits</div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-number">25</div>
                        <div>Repositories</div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-number">50+</div>
                        <div>Stars Earned</div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-number">12</div>
                        <div>Followers</div>
                    </div>
                </div>
            </div>

            <!-- GitHub 잔디 섹션 -->
            <div class="section">
                <div class="section-title">
                    <span class="emoji">📈</span>
                    Contribution Graph
                </div>
                <div class="activity-graph">
                    <div class="graph-placeholder">🌱 GitHub 잔디밭 - 365일 코딩 여정</div>
                    <p style="margin-top: 15px; color: #586069;">연간 커밋 활동을 한눈에 확인하세요</p>
                </div>
            </div>

            <!-- 연락처 섹션 -->
            <div class="section contact-section">
                <div class="section-title">
                    <span class="emoji">📫</span>
                    How to reach me
                </div>
                <div class="contact-links">
                    <a href="mailto:chs010604@gmail.com" class="contact-btn gmail">
                        📧 Gmail
                    </a>
                    <a href="mailto:chs010604@naver.com" class="contact-btn naver">
                        📮 Naver Mail
                    </a>
                </div>
            </div>
            
            <!-- 통계 섹션 -->
            <div class="section stats-section">
                <div class="section-title">
                    <span class="emoji">📊</span>
                    GitHub Stats & Problem Solving
                </div>
                <div class="stats-container">
                    <div class="stat-card">
                        <div class="stat-placeholder">
                            📈 GitHub Stats<br>
                            <small style="font-size: 0.8rem; opacity: 0.8;">
                                실제로는 github-readme-stats API 이미지가 표시됩니다
                            </small>
                        </div>
                        <p><strong>GitHub 활동 통계</strong></p>
                    </div>
                    <div class="stat-card">
                        <div class="stat-placeholder baekjoon-placeholder">
                            🏆 Solved.ac<br>
                            <small style="font-size: 0.8rem; opacity: 0.8;">
                                백준 문제 해결 현황이 표시됩니다
                            </small>
                        </div>
                        <p><strong>알고리즘 문제 해결</strong></p>
                    </div>
                </div>
            </div>
        </div>
        
        <!-- 푸터 -->
        <div class="footer">
            <p>✨ 지속적인 성장을 추구하는 개발자 ✨</p>
            <p style="margin-top: 10px; opacity: 0.7;">GitHub: @hyun1358</p>
        </div>
    </div>
<script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'97127b8f2207ea07',t:'MTc1NTUzMTM0My4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script></body>
</html>
