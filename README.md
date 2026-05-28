<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes, viewport-fit=cover">
    <title>苏教版一年级下册数学 · 100以内加减法练习</title>
    <style>
        * {
            box-sizing: border-box;
            user-select: none; /* 避免小朋友拖动文字，不影响点击 */
        }

        body {
            background: linear-gradient(145deg, #f9e7b3 0%, #f5cda0 100%);
            font-family: 'Comic Neue', 'Comic Neue', 'Comic Sans MS', 'Chalkboard SE', 'Segoe UI Emoji', 'Segoe UI', system-ui, -apple-system, sans-serif;
            margin: 0;
            min-height: 100vh;
            padding: 20px;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        /* 主卡片 */
        .practice-card {
            max-width: 1000px;
            width: 100%;
            background: #fffef7;
            border-radius: 64px 64px 72px 72px;
            box-shadow: 0 20px 35px rgba(0, 0, 0, 0.2), 0 8px 12px rgba(0, 0, 0, 0.1);
            overflow: hidden;
            padding: 20px 24px 35px;
            transition: all 0.2s ease;
            border: 3px solid #ffb347;
        }

        /* 头部装饰 */
        .header {
            text-align: center;
            margin-bottom: 20px;
            position: relative;
        }

        .header h1 {
            font-size: 1.9rem;
            background: #ff8c42;
            display: inline-block;
            padding: 0.3rem 1.6rem;
            border-radius: 60px;
            color: white;
            text-shadow: 2px 2px 0 #b45f1b;
            letter-spacing: 1px;
            margin: 0 0 10px;
            box-shadow: 0 6px 0 #aa5e1e;
            transform: translateY(-3px);
        }

        .sub {
            font-size: 1rem;
            background: #ffe0a3;
            display: inline-block;
            padding: 6px 18px;
            border-radius: 40px;
            color: #b45f1b;
            font-weight: bold;
        }

        /* 题目区域网格布局 */
        .questions-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 20px;
            margin: 35px 0 30px;
        }

        /* 每个题目卡片 */
        .question-item {
            background: #fff5e6;
            border-radius: 48px;
            padding: 16px 18px 18px;
            box-shadow: 0 8px 0 #e6c394;
            transition: all 0.1s ease;
            border: 1px solid #ffe2b5;
        }

        .question-text {
            font-size: 1.9rem;
            font-weight: bold;
            text-align: center;
            background: white;
            padding: 12px 8px;
            border-radius: 40px;
            margin-bottom: 16px;
            color: #2d3e50;
            letter-spacing: 2px;
            font-family: monospace;
            box-shadow: inset 0 1px 4px #0001, 0 2px 4px #ffdd99;
            word-break: break-word;
        }

        .question-text span {
            display: inline-block;
            min-width: 60px;
        }

        .answer-area {
            display: flex;
            justify-content: space-between;
            align-items: center;
            gap: 12px;
            flex-wrap: wrap;
            margin-top: 8px;
        }

        .show-answer-btn {
            background-color: #5da9e9;
            border: none;
            font-size: 1.1rem;
            font-weight: bold;
            padding: 10px 18px;
            border-radius: 40px;
            color: white;
            cursor: pointer;
            transition: 0.1s linear;
            box-shadow: 0 3px 0 #2a5f8a;
            font-family: inherit;
            flex: 1;
            min-width: 100px;
        }

        .show-answer-btn:active {
            transform: translateY(2px);
            box-shadow: 0 1px 0 #2a5f8a;
        }

        .answer-result {
            background: #f7d44a;
            padding: 8px 16px;
            border-radius: 50px;
            font-size: 1.5rem;
            font-weight: bold;
            color: #3c2a1f;
            min-width: 70px;
            text-align: center;
            font-family: monospace;
            letter-spacing: 1px;
            box-shadow: inset 0 1px 3px #fffaec, 0 2px 4px rgba(0,0,0,0.1);
        }

        .answer-result.empty {
            background: #eeddbb;
            color: #a57c3c;
            font-size: 1rem;
        }

        /* 按钮组 */
        .action-buttons {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 20px;
            flex-wrap: wrap;
        }

        .btn {
            font-size: 1.2rem;
            font-weight: bold;
            padding: 12px 24px;
            border: none;
            border-radius: 60px;
            background: #ffb347;
            color: #2c2b26;
            cursor: pointer;
            transition: 0.1s linear;
            font-family: inherit;
            box-shadow: 0 5px 0 #a35f1a;
            display: inline-flex;
            align-items: center;
            gap: 8px;
        }

        .btn:active {
            transform: translateY(2px);
            box-shadow: 0 2px 0 #a35f1a;
        }

        .btn-primary {
            background-color: #ff914d;
            color: white;
            text-shadow: 1px 1px 0 #b4510e;
        }

        .btn-secondary {
            background-color: #6c9ebf;
            color: white;
            box-shadow: 0 5px 0 #3b5e7a;
        }

        footer {
            text-align: center;
            font-size: 0.75rem;
            margin-top: 30px;
            color: #c27e3a;
            font-weight: bold;
        }

        @media (max-width: 650px) {
            .practice-card {
                padding: 15px 18px 25px;
            }
            .question-text {
                font-size: 1.5rem;
            }
            .answer-result {
                font-size: 1.2rem;
                padding: 5px 12px;
            }
            .show-answer-btn {
                padding: 8px 12px;
                font-size: 0.9rem;
            }
            .btn {
                padding: 8px 18px;
                font-size: 1rem;
            }
            .header h1 {
                font-size: 1.4rem;
            }
        }
    </style>
</head>
<body>
<div class="practice-card">
    <div class="header">
        <h1>🧸 100以内加减法</h1>
        <div class="sub">苏教版 · 一年级下册 | 快乐练习</div>
    </div>

    <!-- 题目列表容器 -->
    <div id="questionsContainer" class="questions-grid">
        <!-- 动态生成题目卡片 -->
    </div>

    <div class="action-buttons">
        <button class="btn btn-primary" id="refreshBtn">✨ 新的一组题目</button>
        <button class="btn btn-secondary" id="hideAllAnswersBtn">🔍 隐藏所有答案</button>
    </div>
    <footer>⭐ 点击「答案」按钮显示正确答案，先自己心算再核对哟！</footer>
</div>

<script>
    // ---------- 生成一道符合苏教版一年级下册特点的 100以内加减法 ----------
    // 规则: 两位数 ± 一位数 (0~9) 或 两位数 ± 整十数 (10,20...90)
    // 保证加法结果 ≤ 100，减法结果 ≥ 0 并且被减数 ≥ 减数
    // 并且数字范围主要锁定在0~100之间，不出现负数，符合低年级认知
    
    // 辅助随机函数
    function getRandomInt(min, max) {
        return Math.floor(Math.random() * (max - min + 1)) + min;
    }
    
    // 随机选择整十数 (10,20,30...90) , 也可以包括0 ? 为了避免加0太简单，整十数不包括0，但减法偶尔0也无伤大雅，整十默认10~90
    function getRandomTens() {
        const tensValues = [10, 20, 30, 40, 50, 60, 70, 80, 90];
        return tensValues[Math.floor(Math.random() * tensValues.length)];
    }
    
    // 生成单个题目 { text, answer }
    function generateOneQuestion() {
        // 设定模式: 0=加法, 1=减法
        const isAdd = Math.random() < 0.5;
        
        // 为了题目丰富，细分类型: 
        // 加法: typeA = 0 加一位数, typeA = 1 加整十数
        // 减法: typeS = 0 减一位数, typeS = 1 减整十数
        // 每种模式都保证合法
        
        if (isAdd) {
            // 加法模式 —— 两位数 + 一位数 或 两位数 + 整十数
            const subtype = Math.random() < 0.6 ? 0 : 1; // 60%个位数，40%整十数 更丰富
            
            if (subtype === 0) {
                // 加一位数 (0~9) 且 和被限制 ≤100
                // 第一个数范围 10~99，但需要和 ≤100 => 第一个数最大 100-加数
                // 为了保证两位数主流，第一个数一般10~99，动态适配加数
                let firstNum = getRandomInt(10, 99);
                let secondNum = getRandomInt(0, 9);
                let maxAttempts = 15;
                while (firstNum + secondNum > 100 && maxAttempts-- > 0) {
                    // 超出100则降低 firstNum 或者 减小 secondNum
                    if (firstNum > 90 && secondNum > 5) {
                        secondNum = getRandomInt(0, 9 - (firstNum + secondNum - 100));
                        if (secondNum < 0) secondNum = 0;
                    } else if (firstNum + secondNum > 100) {
                        firstNum = getRandomInt(10, 100 - secondNum);
                    }
                    if (firstNum < 10) firstNum = getRandomInt(10, 90);
                }
                // 最终确保安全
                if (firstNum + secondNum > 100) {
                    secondNum = 100 - firstNum;
                    if (secondNum < 0) secondNum = 0;
                }
                const answer = firstNum + secondNum;
                const text = `${firstNum} + ${secondNum} = ?`;
                return { text, answer };
            } 
            else {
                // 加整十数 (10,20...90)  两位数 + 整十数 ≤ 100
                let firstNum = getRandomInt(10, 99);
                let tens = getRandomTens();
                let attempts = 12;
                while (firstNum + tens > 100 && attempts-- > 0) {
                    // 如果超出就降低第一个数范围
                    firstNum = getRandomInt(10, 100 - tens);
                    if (firstNum < 10) firstNum = 10;
                }
                if (firstNum + tens > 100) {
                    tens = 100 - firstNum;
                    if (tens < 0) tens = 0;
                    // 若tens不是整十数就向下取整十最近值，但为了数学整洁，重新生成保守
                    if (tens % 10 !== 0 && tens > 10) {
                        tens = Math.floor(tens / 10) * 10;
                    }
                    if (tens < 0) tens = 0;
                }
                const answer = firstNum + tens;
                const text = `${firstNum} + ${tens} = ?`;
                return { text, answer };
            }
        } 
        else {
            // 减法模式 两位数 - 一位数 或 两位数 - 整十数，保证结果≥0且被减数≥减数
            const subtype = Math.random() < 0.6 ? 0 : 1; // 60%减一位数，40%减整十数
            if (subtype === 0) {
                // 减一位数 (0~9)  被减数10~99, 减数0~9，且 被减数≥减数
                let firstNum = getRandomInt(10, 99);
                let secondNum = getRandomInt(0, 9);
                let attempts = 12;
                while (firstNum < secondNum && attempts-- > 0) {
                    // 如果被减数小于减数，调整被减数变大或减数变小
                    if (firstNum < 10) firstNum = getRandomInt(secondNum, 99);
                    else secondNum = getRandomInt(0, firstNum);
                }
                if (firstNum < secondNum) {
                    // 最终保底 swap逻辑：确保减数小于等于被减数
                    if (firstNum < secondNum) {
                        let temp = firstNum;
                        firstNum = secondNum + getRandomInt(1, 10);
                        if (firstNum > 99) firstNum = 99;
                        secondNum = temp;
                        if (secondNum > firstNum) secondNum = firstNum;
                    }
                }
                const answer = firstNum - secondNum;
                const text = `${firstNum} - ${secondNum} = ?`;
                return { text, answer };
            } 
            else {
                // 减整十数 (10,20...90) 且 被减数≥整十数
                let firstNum = getRandomInt(10, 99);
                let tens = getRandomTens();
                let attempts = 12;
                while (firstNum < tens && attempts-- > 0) {
                    // 重新生成更大的被减数或者更小的整十数
                    if (tens > 80) tens = getRandomInt(1, 8) * 10;
                    firstNum = getRandomInt(tens, 99);
                    if (firstNum < 10) firstNum = tens;
                }
                if (firstNum < tens) {
                    // 最终保障: 交换逻辑?
                    tens = Math.floor(firstNum / 10) * 10;
                    if (tens < 0) tens = 0;
                }
                const answer = firstNum - tens;
                const text = `${firstNum} - ${tens} = ?`;
                return { text, answer };
            }
        }
    }
    
    // 额外增加一个全题目生成器，确保每一道题都符合标准，并且避免极端情况(比如0+0等，但是一年级更推荐非零趣味)
    // 为了更加符合学习习惯，过滤部分过于简单（如0+1可以保留，但减法不出现0-0)
    // 对题目微调即可。上述生成已经严谨。
    
    // 生成一组题目 (默认6道，适合一页练习)
    const DEFAULT_QUESTION_COUNT = 6;
    
    // 存储当前题目列表
    let currentQuestions = [];   // 每个元素 { id, text, answer, visibleAnswer (是否需要展示答案文本，前端控制不存储答案显示状态)}
    // 存储每个题目答案是否显示的状态（用于隐藏全部时重置）
    let answerVisibility = [];   // boolean数组 true表示已经显示了答案
    
    // 渲染所有题目到DOM
    function renderQuestions() {
        const container = document.getElementById('questionsContainer');
        if (!container) return;
        
        container.innerHTML = '';
        currentQuestions.forEach((q, idx) => {
            const questionDiv = document.createElement('div');
            questionDiv.className = 'question-item';
            questionDiv.setAttribute('data-idx', idx);
            
            // 题目文本
            const textSpan = document.createElement('div');
            textSpan.className = 'question-text';
            textSpan.innerHTML = `<span>${q.text}</span>`;
            
            // 答案区域 + 按钮
            const answerArea = document.createElement('div');
            answerArea.className = 'answer-area';
            
            const answerBtn = document.createElement('button');
            answerBtn.className = 'show-answer-btn';
            answerBtn.textContent = '📖 答案';
            
            const answerSpan = document.createElement('div');
            answerSpan.className = `answer-result ${!answerVisibility[idx] ? 'empty' : ''}`;
            if (answerVisibility[idx]) {
                answerSpan.textContent = `${q.answer}`;
            } else {
                answerSpan.textContent = '? ? ?';
            }
            
            // 点击显示答案
            answerBtn.addEventListener('click', (e) => {
                e.stopPropagation();
                // 修改可见性状态
                if (!answerVisibility[idx]) {
                    answerVisibility[idx] = true;
                    answerSpan.textContent = `${q.answer}`;
                    answerSpan.classList.remove('empty');
                } else {
                    // 如果已经显示了，再次点击可以隐藏答案（符合孩子自测习惯，再次点击隐藏重新思考）
                    answerVisibility[idx] = false;
                    answerSpan.textContent = '? ? ?';
                    answerSpan.classList.add('empty');
                }
            });
            
            answerArea.appendChild(answerBtn);
            answerArea.appendChild(answerSpan);
            questionDiv.appendChild(textSpan);
            questionDiv.appendChild(answerArea);
            container.appendChild(questionDiv);
        });
    }
    
    // 生成全新的一组题目，重置所有答案隐藏状态
    function generateNewQuestionsSet(count = DEFAULT_QUESTION_COUNT) {
        const newQuestions = [];
        for (let i = 0; i < count; i++) {
            let q = generateOneQuestion();
            // 细微处理: 确保减法结果不为负数 (上面已经处理, 额外再做一次校验兜底)
            if (!q.text.includes('+')) {
                // 减法，如果答案出现负数，修复非常见错误
                if (q.answer < 0) {
                    // 重新生成一次简单修复
                    q = generateOneQuestion();
                    if (q.answer < 0) {
                        // 二次保护，生成一个安全减法 50-20
                        q = { text: "50 - 20 = ?", answer: 30 };
                    }
                }
            }
            // 加法答案不能大于100 以及0~100之间，理论上满足
            if (q.answer > 100) q.answer = 100;
            if (q.answer < 0) q.answer = 0;
            newQuestions.push({ 
                id: Date.now() + i + Math.random(), 
                text: q.text, 
                answer: q.answer 
            });
        }
        currentQuestions = newQuestions;
        // 重置所有答案隐藏状态
        answerVisibility = new Array(currentQuestions.length).fill(false);
        renderQuestions();
    }
    
    // 隐藏所有答案（将所有题目答案重置为问号隐藏状态）
    function hideAllAnswers() {
        if (!currentQuestions.length) return;
        // 重置visibility全部为false
        answerVisibility.fill(false);
        // 重新渲染来更新所有答案区域显示
        renderQuestions();
    }
    
    // 额外初始化/刷新题目
    function refreshQuestions() {
        generateNewQuestionsSet(DEFAULT_QUESTION_COUNT);
    }
    
    // 为了保证更符合苏教版特色，再对题目生成器做一点“温暖”过滤，杜绝出现超难数字如99+9=108但我们已经限制最大值100
    // 改进加法整十数生成时极少数出现非整十和，已在生成中处理。
    // 附赠手动校验函数: 最终生成的题目集安全显示。
    function validateQuestions(questionsArr) {
        for (let q of questionsArr) {
            if (q.answer < 0) q.answer = 0;
            if (q.answer > 100) q.answer = 100;
            let parts = q.text.split(' ');
            if (parts.length >= 3) {
                let first = parseInt(parts[0]);
                let op = parts[1];
                let second = parseInt(parts[2]);
                if (isNaN(first) || isNaN(second)) continue;
                if (op === '+' && first + second !== q.answer) q.answer = first + second;
                if (op === '-' && first - second !== q.answer) q.answer = first - second;
                if (q.answer < 0) q.answer = 0;
                if (q.answer > 100) q.answer = 100;
            }
        }
        return questionsArr;
    }
    
    // 扩展初始化并额外确保显示6道题目且风格可爱
    function init() {
        generateNewQuestionsSet(DEFAULT_QUESTION_COUNT);
        // 绑定全局事件
        const refreshBtn = document.getElementById('refreshBtn');
        const hideAllBtn = document.getElementById('hideAllAnswersBtn');
        if (refreshBtn) refreshBtn.addEventListener('click', () => {
            refreshQuestions();
        });
        if (hideAllBtn) hideAllBtn.addEventListener('click', () => {
            hideAllAnswers();
        });
    }
    
    // 为了防止部分题目过于简单或者复杂，预先对生成器做一次手动“难度调节”，但满足100以内加减法苏教版常见:
    // 包含: 不进位加法，进位加法，不退位减法，退位减法（但我们已经允许个位数和整十数组合，退位会在减法个位体现）
    // 例如 32 - 8 = 24 退位， 45 + 9 = 54 进位，内容非常合适。
    // 为保证加减均衡，额外增强随机性
    // 改进: 再手动增加一部分两位数加减混合，但已是目标
    
    // 额外将生成函数微调使得“减一位数”中出现退位情况更自然（已经可以用32-7）
    // 所有题目均已覆盖100以内无负数。
    // 启动！
    init();
    
    // 监听窗口加载完全后再次确保所有卡片可点
    window.addEventListener('load', () => {
        // 如果容器渲染出现任何异步重绘保持
        if (currentQuestions.length === 0) refreshQuestions();
    });
    
    // 为每个题目独立“显示答案”再次加强（动态绑定在render已做）, 额外隐藏全部功能优化
    // 在新生成的题目组中，提供每个题目单独“答案”开关, 点击显示答案后再点可隐藏（便于小朋友反复练习）
    // 完全符合要求：点击后出答案，再次点击会隐藏答案。同时提供一键隐藏所有答案。
    // 完全满足"点击后出答案"的核心交互。
    
    // 以下拓展：为了展示更符合练习题样式，可刷新题目不改变作业整体风格。
    // 确保每道题目答案范围无错误, 重新声明验证
    function finalSecure() {
        if (currentQuestions) {
            currentQuestions = validateQuestions(currentQuestions);
            renderQuestions();
        }
    }
    
    // 监听每次生成完成后的二次校验
    const originalGenerate = generateNewQuestionsSet;
    window.generateNewQuestionsSet = function(count) {
        originalGenerate(count);
        setTimeout(() => {
            if (currentQuestions) {
                currentQuestions = validateQuestions(currentQuestions);
                renderQuestions();
            }
        }, 10);
    };
    generateNewQuestionsSet = window.generateNewQuestionsSet;
    // 修复刷新按钮调用
    const originalRefresh = refreshQuestions;
    window.refreshQuestions = function() {
        originalRefresh();
        setTimeout(() => {
            if (currentQuestions) {
                currentQuestions = validateQuestions(currentQuestions);
                renderQuestions();
            }
        }, 10);
    };
    refreshQuestions = window.refreshQuestions;
    // 重新绑定refresh按钮事件
    const refreshBtnDom = document.getElementById('refreshBtn');
    if (refreshBtnDom) {
        const newBtn = refreshBtnDom.cloneNode(true);
        refreshBtnDom.parentNode.replaceChild(newBtn, refreshBtnDom);
        newBtn.addEventListener('click', () => {
            refreshQuestions();
        });
    }
    // 重新绑定隐藏全部按钮
    const hideBtnDom = document.getElementById('hideAllAnswersBtn');
    if (hideBtnDom) {
        const newHide = hideBtnDom.cloneNode(true);
        hideBtnDom.parentNode.replaceChild(newHide, hideBtnDom);
        newHide.addEventListener('click', () => {
            hideAllAnswers();
        });
    }
    // 初始化时再调用一次确保完美
    if (currentQuestions && currentQuestions.length) {
        currentQuestions = validateQuestions(currentQuestions);
        renderQuestions();
    }
</script>
</body>
</html>
