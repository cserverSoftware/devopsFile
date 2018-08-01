pipeline {
  agent any
  stages {
    //检出阶段开始
    stage('check out') { 
      parallel {
        stage('check out') {
          steps {
            echo 'check out'
          }
        }
        stage('parallel1ofcheck out') {
          steps {
            echo 'parallel1ofcheck out'
          }
        }
        stage('parallel2ofcheck out') {
          steps {
            echo 'parallel2ofcheck out'
          }
        }
        stage('parallel3ofcheck out') {
          steps {
            echo 'parallel3ofcheck out'
          }
        }
      }
    } //检出阶段结束
     //构建阶段开始
    stage('build') {
      parallel {
        stage('build') {
          steps {
            echo 'build'
          }
        }
        stage('Paralle1OfBuild') {
          steps {
            echo 'Paralle1OfBuild'
          }
        }
      }
    } //构建阶段结束
  }
}
