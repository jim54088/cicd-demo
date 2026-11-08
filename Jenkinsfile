pipeline {
    agent any                       // 為什麼:在哪台機器跑都行,這裡就是 Jenkins 自己的容器
    stages {
        stage('Test') {             // 為什麼:一個 stage = 一個步驟,畫面上會分段顯示紅綠
            steps {
                // 為什麼用 venv:避免汙染系統 Python,每次都是乾淨環境
                sh '''
                    python3 -m venv venv
                    . venv/bin/activate
                    pip install pytest
                    pytest
                '''
            }
        }
    }
}
