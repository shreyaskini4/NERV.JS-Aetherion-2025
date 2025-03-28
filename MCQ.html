<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MCQ Quiz Application</title>
    <link rel="stylesheet" href="style.css">
    <style>
        body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    line-height: 1.6;
    color: #333;
    max-width: 800px;
    margin: 0 auto;
    padding: 20px;
    background-color: #f5f5f5;
}

.quiz-container {
    background-color: white;
    padding: 30px;
    border-radius: 10px;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
}

h1, h2 {
    color: #2c3e50;
    text-align: center;
}

.question {
    margin-bottom: 25px;
    padding: 20px;
    border: 1px solid #e0e0e0;
    border-radius: 8px;
    background-color: #f9f9f9;
}

.options {
    margin-left: 15px;
}

.option {
    margin: 12px 0;
}

input[type="radio"] {
    margin-right: 10px;
}

button {
    background-color: #3498db;
    color: white;
    padding: 12px 24px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    font-size: 16px;
    display: block;
    margin: 30px auto 0;
    transition: background-color 0.3s;
}

button:hover {
    background-color: #2980b9;
}

.hidden {
    display: none;
}

.correct {
    color: #27ae60;
    font-weight: bold;
}

.incorrect {
    color: #e74c3c;
}

#answerFeedback {
    margin-top: 20px;
}

.feedback-item {
    margin-bottom: 15px;
    padding: 10px;
    border-left: 4px solid #ddd;
}

.correct .feedback-item {
    border-left-color: #27ae60;
}

.incorrect .feedback-item {
    border-left-color: #e74c3c;
}

#scoreDisplay {
    font-size: 24px;
    text-align: center;
    margin: 20px 0;
    padding: 15px;
    background-color: #f8f9fa;
    border-radius: 5px;
}
    </style>
</head>
<body>
    <script>
        document.addEventListener('DOMContentLoaded', () => {
    const quizForm = document.getElementById('quizForm');
    const questionsContainer = document.getElementById('questionsContainer');
    const resultContainer = document.getElementById('resultContainer');
    const scoreDisplay = document.getElementById('scoreDisplay');
    const answerFeedback = document.getElementById('answerFeedback');

    // Quiz questions data
    const quizData = [
        {
            question: "What is the capital of France?",
            options: ["London", "Paris", "Berlin", "Madrid"],
            correctAnswer: 1
        },
        {
            question: "Which planet is known as the Red Planet?",
            options: ["Venus", "Mars", "Jupiter", "Saturn"],
            correctAnswer: 1
        },
        {
            question: "What is the largest mammal in the world?",
            options: ["Elephant", "Blue Whale", "Giraffe", "Polar Bear"],
            correctAnswer: 1
        },
        {
            question: "Who painted the Mona Lisa?",
            options: [
                "Vincent van Gogh",
                "Pablo Picasso",
                "Leonardo da Vinci",
                "Michelangelo"
            ],
            correctAnswer: 2
        },
        {
            question: "What is the chemical symbol for gold?",
            options: ["Go", "Gd", "Au", "Ag"],
            correctAnswer: 2
        }
    ];

    // Render questions
    quizData.forEach((q, index) => {
        const questionDiv = document.createElement('div');
        questionDiv.className = 'question';
        questionDiv.innerHTML = `
            <p>${index + 1}. ${q.question}</p>
            <div class="options">
                ${q.options.map((option, i) => `
                    <div class="option">
                        <input type="radio" name="q${index}" id="q${index}o${i}" value="${i}">
                        <label for="q${index}o${i}">${option}</label>
                    </div>
                `).join('')}
            </div>
        `;
        questionsContainer.appendChild(questionDiv);
    });

    // Handle form submission
    quizForm.addEventListener('submit', async (e) => {
        e.preventDefault();
        
        let score = 0;
        const userAnswers = [];
        const totalQuestions = quizData.length;
        
        // Check answers and collect responses
        quizData.forEach((q, index) => {
            const selectedOption = document.querySelector(`input[name="q${index}"]:checked`);
            const userAnswer = selectedOption ? parseInt(selectedOption.value) : null;
            const isCorrect = userAnswer === q.correctAnswer;
            
            if (isCorrect) score++;
            
            userAnswers.push({
                question: q.question,
                userAnswer: userAnswer !== null ? q.options[userAnswer] : "Not answered",
                correctAnswer: q.options[q.correctAnswer],
                isCorrect: isCorrect
            });
        });
        
        // Calculate percentage
        const percentage = Math.round((score / totalQuestions) * 100);
        
        // Display results
        scoreDisplay.innerHTML = `You scored ${score} out of ${totalQuestions} (${percentage}%)`;
        
        // Show answer feedback
        answerFeedback.innerHTML = userAnswers.map((ans, i) => `
            <div class="feedback-item ${ans.isCorrect ? 'correct' : 'incorrect'}">
                <p><strong>Question ${i + 1}:</strong> ${ans.question}</p>
                <p>Your answer: ${ans.userAnswer}</p>
                ${!ans.isCorrect ? `<p>Correct answer: ${ans.correctAnswer}</p>` : ''}
            </div>
        `).join('');
        
        // Show result container
        resultContainer.classList.remove('hidden');
        
        // Scroll to results
        resultContainer.scrollIntoView({ behavior: 'smooth' });
        
        // Send results to backend
        try {
            const response = await fetch('/api/results', {
                method: 'POST',
                headers: {
                    'Content-Type': 'application/json',
                },
                body: JSON.stringify({
                    score,
                    totalQuestions,
                    percentage,
                    answers: userAnswers,
                    timestamp: new Date().toISOString()
                })
            });
            
            if (!response.ok) {
                throw new Error('Failed to save results');
            }
            
            console.log('Results saved successfully');
        } catch (error) {
            console.error('Error saving results:', error);
        }
    });
});
    </script>
    <div class="quiz-container">
        <h1>Knowledge Test</h1>
        <form id="quizForm">
            <!-- Questions will be inserted here by JavaScript -->
            <div id="questionsContainer"></div>
            <button type="submit" id="submitBtn">Submit Quiz</button>
        </form>
        <div id="resultContainer" class="hidden">
            <h2>Your Results</h2>
            <div id="scoreDisplay"></div>
            <div id="answerFeedback"></div>
        </div>
    </div>
    <script src="script.js"></script>
</body>
</html>