pipeline {
  agent any
  stages {
    //检出阶段开始
    stage('检出') { 
      parallel {
        
        stage('检测代码') {
          steps {
            echo 'parallel1ofcheck out'
          }
        }
        stage('准备检出') {
          steps {
            echo 'parallel2ofcheck out'
          }
        }
        stage('检出完成') {
          steps {
            echo 'parallel3ofcheck out'
          }
        }
      }
    } //检出阶段结束
     //构建阶段开始
    stage('构建') {
      parallel {
        stage('build') {
          steps {
            echo 'build'
          }
        }
        stage('开始构建') {
          steps {
            echo 'Paralle1OfBuild'
          }
        }
      }
    } //构建阶段结束
  }
}
