
# Publish code coverage in nocodDB and CodeCov using CompositeAction

## Step 1
Add [CompositeAction.yml](https://github.com/atacama-blooms-gmbh-co-kg/sbt-codecoverage-template/blob/935bfdd01aa506e2844d9dd977eabaa2d2339551/.github/workflows/CompositeAction.yml) to your workflow of your desired repository. You have to configure, according to your project type. 

The major changes, you have to make in these set of codes. for example if you are working on Gradle project, then you have change test command to __./gradlew test__

![Image](https://github.com/atacama-blooms-gmbh-co-kg/codecoverage-nocodb-publish-action/blob/0d89231ad03cc2ceea384577d13a64bdce2dfdb8/Screenshots/Major%20changes.png)

Here you also need to change the values in the input, depending upon your code coverage format and project type.

![Image](https://github.com/atacama-blooms-gmbh-co-kg/codecoverage-nocodb-publish-action/blob/5363e10f4883b312027f15a1f68e3224ca61e915/Screenshots/Major%20changes%202.png)

## Step2 
Add your desired repository to codecov server in order to get CodeCov token.![Image](https://github.com/atacama-blooms-gmbh-co-kg/codecoverage-nocodb-publish-action/blob/0d89231ad03cc2ceea384577d13a64bdce2dfdb8/Screenshots/Add%20Repo%20to%20CodeCov.png)

## Step 3
Add codecov token as repository secret, to push code coverage to the CodeCov Server.![Image](https://github.com/atacama-blooms-gmbh-co-kg/codecoverage-nocodb-publish-action/blob/8ddf3d7fb7dc2b5754dd6ba75d713e8ded42e93c/Screenshots/CodeCov%20Token.png)


