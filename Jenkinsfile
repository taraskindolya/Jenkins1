pipeline {
  agent {
    node {
      label 'master_lable'
    }
  }
    stages {
	 stage("Init") {
         steps {
            echo "1111111111"
		 }
	 }
        stage("Release workflow") {
            parallel {
                   stage("Analysis") {
                            steps {
                                echo "444444444444"
                            }
                        }
     
                stage("Phase 1") {
                    stages {
                        stage("Build") {
                            steps {
                                echo "2222222222222"
                            }
                        }
                        stage("Testing") {
                            steps {
                                echo "3333333333"
									}
								}
                            }
                        }
                    }
                }

	 stage("Release") {
         steps {
            echo "66666666666"
		 }
	  }
   }
}
