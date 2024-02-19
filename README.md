# Publish code coverage in nocodDB and CodeCov for scala projects

# Step 1
Add [this](https://github.com/atacama-blooms-gmbh-co-kg/codecoverage-nocodb-publish-action/blob/e6f3c4685ab4fabb240bf843e7ba843252570a9c/NocoDB-CodeCov.yml) snippet to your workflow of the repo. You can configure it if you need to change anything. 

With different coverage output formats, such as JacocoReport
To Extract line coverage from the Jacoco report, you can try this. If it does not work, then you have to look at keywords and fields in your report and make changes in this line accordingly.

COVERAGE_PERCENTAGE=$(cat build/reports/jacoco/test/jacocoTestReport.xml | grep -oP 'counter type="LINE" missed="\K[^"]*' | awk -F'"' '{covered+=$2; missed+=$4} END {print covered/(covered+missed)*100}')

# Step2 

Add repository token as repository secret, to push code coverage to the CodeCov Server. Once you have the credentials for it, you can easily find the token in CodeCov.

You can find a set of codes to upload coverage to CodeCov in Workflows.

# Screenshot
![image](https://github.com/atacama-blooms-gmbh-co-kg/codecoverage-nocodb-publish-action/blob/0a31fdbd81d923f845ef6608ef9740c95fbd5e86/CodeCov.png)
