// 题库配置
const questionBank = [
  {
    question: "中国绘画中 ()地位最高。",
    options: ["A、山水画", "B、人物画", "C、花鸟画", "D、器物画"],
    answer: "A"
  },
  {
    question: "中国最好的砚出自以下哪个省 20C",
    options: ["A、山西省", "B、安徽省", "C、广东省", "D、山东省"],
    answer: "C"
  },
  {
    question: "关于西方绘画说法正确的是 ()。",
    options: ["A、西方绘画更注重精神世界", "B、西方绘画注重再现", "C、西方绘画注重", "D、西方绘画更注重物质世界"],
    answer: ["A", "C", "D"]
  },
  {
    question: "中国绘画注重山水和花鸟。 （）对",
    answer: true
  },
  {
    question: "中国绘画讲究明暗色彩。 0X",
    answer: false
  },
  {
    question: "西方美术是怎样的(二)",
    options: ["A、写物像物", "B、随类赋彩", "C、气韵生动", "D、传移摸写"],
    answer: "C"
  },
  {
    question: "中国绘画最重要的审美元素是 (0。D",
    options: ["A、明暗", "B、色彩", "C、光影", "D、线条"],
    answer: "D"
  },
  {
    question: "中国画家认为轮廓线有什么功能 ?0C",
    options: ["A、抒情和审美", "B、描物与审美", "C、描物与抒情"],
    answer: "C"
  }
];

// 处理器函数，根据题库配置返回题目和答案
const questionHandler = (title, type, options) => {
  const question = questionBank.find(item => item.question === title);
  if (question) {
    if (type === "multiple") {
      // 多选题，返回二维数组
      return question.answer.map(answer => [title, answer]);
    } else {
      // 单选题或判断题，返回单一数组
      return [title, question.answer];
    }
  } else {
    return undefined;
  }
};

// 示例调用
defaultAnswerWrapperHandler(
  {
    title: '中国绘画中 ()地位最高。',
    type: 'single',
    options: 'A、山水画\nB、人物画\nC、花鸟画\nD、器物画'
  },
  [
    {
      url: "https://your-custom-url.com/search",
      method: "get",
      contentType: "json",
      data: {
        title: "${title}",
        customParam: "123"
      },
      handler: "return questionHandler('${title}', '${type}', '${options}')"
    },
  ]
);
