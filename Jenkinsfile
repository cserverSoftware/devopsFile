pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        echo 'Checkout'
        checkout([$class: 'SubversionSCM', additionalCredentials: [], excludedCommitMessages: '', excludedRegions: '', excludedRevprop: '', excludedUsers: '', filterChangelog: false, ignoreDirPropChanges: false, includedRegions: '', locations: [[cancelProcessOnExternalsFail: true, credentialsId: 'dafdb735-7cae-4d2d-a459-609a3f4f98e1', depthOption: 'infinity', ignoreExternalsOption: true, local: '.', remote: 'https://192.168.1.15/svn/saasshop/trunk/source/SaaS']], quietOperation: false, workspaceUpdater: [$class: 'UpdateUpdater']])
      }
    }
  }
  parameters {
    string(name: 'DeployENV', defaultValue: 'pre', description: '''请输入构建包的目标环境：
1.输入[pre]公司内部预发布环境包
2.输入[cserver]，中服正式
3.输入[gyy],西安工业云
4.输入[gyypre],西安工业云预发布环境''')
    string(name: 'VERSION', defaultValue: '', description: '''请输入发布包版本号。
格式规范：应用名称-版本号-时间，如：SAASSHOP-1.0-20180705表示软件超市1.0版本,创建日期为2018年7月5日''')
  }
}