Codebase Analysis for: java/file-generator-engine

Directory Structure:
└── file-generator-engine
    ├── Dockerfile
    ├── target
    │   ├── test-classes
    │   │   ├── empty_template.xlsx
    │   │   ├── salary_update_template.xlsx
    │   │   └── com
    │   │       └── papaya
    │   │           └── file_generator
    │   │               ├── engine
    │   │               │   ├── configuration
    │   │               │   │   └── FileGeneratorHandlerConfigurationTest.class
    │   │               │   └── service
    │   │               │       └── FileGeneratorServiceTest.class
    │   │               └── handlers
    │   │                   └── template_based_excel
    │   │                       ├── TemplateBasedExcelHandlerTest.class
    │   │                       └── JsonGenerator.class
    │   ├── generated-sources
    │   │   └── annotations
    │   ├── classes
    │   │   ├── application-local.properties
    │   │   ├── handlers.properties
    │   │   ├── com
    │   │   │   └── papaya
    │   │   │       └── file_generator
    │   │   │           ├── engine
    │   │   │           │   ├── configuration
    │   │   │           │   │   └── FileGeneratorHandlerConfiguration.class
    │   │   │           │   ├── FileGeneratorEngineApplication.class
    │   │   │           │   ├── util
    │   │   │           │   │   └── StackTraceConverter.class
    │   │   │           │   ├── queue
    │   │   │           │   │   ├── handler
    │   │   │           │   │   │   └── main
    │   │   │           │   │   │       ├── MessageTypeConstants.class
    │   │   │           │   │   │       └── FileGeneratorEventHandler.class
    │   │   │           │   │   ├── producer
    │   │   │           │   │   │   └── DefaultProducer.class
    │   │   │           │   │   ├── connection
    │   │   │           │   │   │   ├── ConsumerConnection.class
    │   │   │           │   │   │   └── ProducerConnection.class
    │   │   │           │   │   ├── model
    │   │   │           │   │   │   └── GenerateCommandDTO.class
    │   │   │           │   │   └── consumer
    │   │   │           │   │       └── DefaultConsumer.class
    │   │   │           │   └── service
    │   │   │           │       └── FileGeneratorService.class
    │   │   │           └── handlers
    │   │   │               └── template_based_excel
    │   │   │                   ├── utils
    │   │   │                   │   ├── parser_strategy
    │   │   │                   │   │   ├── TableExcelReplacementStrategy.class
    │   │   │                   │   │   ├── ValueReplacementStrategyFactory.class
    │   │   │                   │   │   ├── ExcelWithFormatReplacementStrategy.class
    │   │   │                   │   │   └── ExcelReplacementStrategy.class
    │   │   │                   │   ├── JsonDataParser.class
    │   │   │                   │   └── ExcelGenerator.class
    │   │   │                   ├── TemplateBasedExcelHandler.class
    │   │   │                   └── model
    │   │   │                       ├── Properties.class
    │   │   │                       ├── ExcelCellTableValueDTO.class
    │   │   │                       ├── PlaceholderPosition.class
    │   │   │                       ├── ExcelCellFormattedValueDTO.class
    │   │   │                       ├── SheetPropertiesDTO.class
    │   │   │                       ├── ExcelCellValueTypeIdResolver.class
    │   │   │                       ├── ColumnPropertiesDTO.class
    │   │   │                       ├── ExcelSheetDTO.class
    │   │   │                       ├── ExcelCellDTO.class
    │   │   │                       └── ExcelFileDTO.class
    │   │   └── application.properties
    │   └── generated-test-sources
    │       └── test-annotations
    ├── CODEOWNERS
    ├── .github
    │   ├── dependabot.yaml
    │   ├── workflows
    │   │   ├── run-tests.yaml
    │   │   ├── manual-deploy.yaml
    │   │   └── deploy.yaml
    │   ├── README.md
    │   └── cicd-doc.md
    ├── docker-compose.yml
    ├── test1.xlsx
    ├── compose-dev.yaml
    └── src
        ├── test
        │   ├── resources
        │   │   ├── empty_template.xlsx
        │   │   ├── salary_update_template.xlsx
        │   │   └── test1.xlsx
        │   └── java
        │       └── com
        │           └── papaya
        │               └── file_generator
        │                   ├── engine
        │                   │   ├── configuration
        │                   │   │   └── FileGeneratorHandlerConfigurationTest.java
        │                   │   └── service
        │                   │       └── FileGeneratorServiceTest.java
        │                   └── handlers
        │                       └── template_based_excel
        │                           ├── TemplateBasedExcelHandlerTest.java
        │                           └── JsonGenerator.java
        └── main
            ├── resources
            │   ├── application-local.properties
            │   ├── handlers.properties
            │   └── application.properties
            └── java
                └── com
                    └── papaya
                        ├── file_generator
                        │   ├── engine
                        │   │   ├── configuration
                        │   │   │   └── FileGeneratorHandlerConfiguration.java
                        │   │   ├── util
                        │   │   │   └── StackTraceConverter.java
                        │   │   ├── queue
                        │   │   │   ├── handler
                        │   │   │   │   └── main
                        │   │   │   │       ├── FileGeneratorEventHandler.java
                        │   │   │   │       └── MessageTypeConstants.java
                        │   │   │   ├── producer
                        │   │   │   │   └── DefaultProducer.java
                        │   │   │   ├── connection
                        │   │   │   │   ├── ProducerConnection.java
                        │   │   │   │   └── ConsumerConnection.java
                        │   │   │   ├── model
                        │   │   │   │   └── GenerateCommandDTO.java
                        │   │   │   └── consumer
                        │   │   │       └── DefaultConsumer.java
                        │   │   ├── service
                        │   │   │   └── FileGeneratorService.java
                        │   │   └── FileGeneratorEngineApplication.java
                        │   └── handlers
                        │       └── template_based_excel
                        │           ├── utils
                        │           │   ├── parser_strategy
                        │           │   │   ├── ExcelReplacementStrategy.java
                        │           │   │   ├── TableExcelReplacementStrategy.java
                        │           │   │   ├── ValueReplacementStrategyFactory.java
                        │           │   │   └── ExcelWithFormatReplacementStrategy.java
                        │           │   ├── JsonDataParser.java
                        │           │   └── ExcelGenerator.java
                        │           ├── model
                        │           │   ├── ExcelSheetDTO.java
                        │           │   ├── ExcelCellValueTypeIdResolver.java
                        │           │   ├── ExcelCellFormattedValueDTO.java
                        │           │   ├── PlaceholderPosition.java
                        │           │   ├── ExcelCellTableValueDTO.java
                        │           │   ├── ColumnPropertiesDTO.java
                        │           │   ├── Properties.java
                        │           │   ├── ExcelFileDTO.java
                        │           │   ├── SheetPropertiesDTO.java
                        │           │   └── ExcelCellDTO.java
                        │           └── TemplateBasedExcelHandler.java
                        └── filegenerator
                            └── engine
                                └── queue
                                    └── consumer

Summary:
Total files analyzed: 86
Total directories analyzed: 74
Estimated output size: 86.65 KB
Actual analyzed size: 3001.91 KB
Total tokens: 16475
Actual text content size: 80.98 KB

File Contents:

==================================================
File: file-generator-engine/Dockerfile
==================================================
FROM openjdk:17-slim-buster
RUN  apt-get update \
     && apt install -y fontconfig libfreetype6

EXPOSE 8120

RUN groupadd -g 1000 cmuser
RUN useradd -u 1000 -g cmuser cmuser

COPY ./target/file-generator-engine-0.0.1.jar /usr/app/application.jar

WORKDIR /usr/app
EXPOSE 9999

ENTRYPOINT ["java", "-jar", "application.jar"]


==================================================
File: file-generator-engine/target/classes/application-local.properties
==================================================
logging.level.web=info
logging.config=classpath:logback-spring.xml

server.port=8120
server.servlet.context-path=/file-generator-engine

rabbitmq.url=amqp://localhost/papaya
rabbitmq.enabled=true
rabbitmq.exchange=file_generator.tx
rabbitmq.queue=file-generator.q

amazon.bucket.name=papaya-file-generator-integration
amazon.region.name=eu-west-1
amazon.file.expiration.time=86400000
amazon.folder.name=generated-files/

management.endpoints.web.exposure.include=health
xml.file.max.row.count=201



==================================================
File: file-generator-engine/target/classes/handlers.properties
==================================================
handler.excel-template=com.papaya.file_generator.handlers.template_based_excel.TemplateBasedExcelHandler
handler.template=com.papaya.file_generator.handlers.template_based_excel.TemplateBasedExcelHandler


==================================================
File: file-generator-engine/target/classes/application.properties
==================================================
logging.level.web=info
logging.config=classpath:logback-spring.xml

server.port=8120
server.servlet.context-path=/file-generator-engine

rabbitmq.enabled=true
rabbitmq.exchange=file_generator.tx
rabbitmq.queue=file-generator.q


amazon.region.name=eu-west-1

management.endpoints.web.exposure.include=health
management.endpoint.metrics.enabled=true


management.statsd.metrics.export.enabled=true
management.statsd.metrics.export.port=8125
management.metrics.tags.service="file-generator-engine"
xml.file.max.row.count=201



==================================================
File: file-generator-engine/CODEOWNERS
==================================================
# GitHub Docs https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-code-owners

* @papayaglobal/papaya-infra


==================================================
File: file-generator-engine/.github/dependabot.yaml
==================================================
version: 2
updates:
  - package-ecosystem: maven
    directory: "/"
    open-pull-requests-limit: 3
    schedule:
      interval: "weekly"


==================================================
File: file-generator-engine/.github/workflows/run-tests.yaml
==================================================
name: Tests

on:
  workflow_call:
  pull_request:
    types: [opened, edited, synchronize]
    paths-ignore:
      - '**.md'
      - '**/*.md'
      - '**/.gitignore'
      - '.gitignore'
      - '**/CODEOWNERS'
      - 'CODEOWNERS'
      - '**/.dockerignore'
      - '.dockerignore'

jobs:
  SAST:
    uses: papayaglobal/workflows/.github/workflows/semgrep.yaml@main
    secrets: inherit
  Tests:
    uses: papayaglobal/workflows/.github/workflows/tests.yaml@main
    with:
      java-ver: 17
      distribution: 'temurin'
      account: core
      allure-testresults-path: allure-reports/test
    secrets: inherit


==================================================
File: file-generator-engine/.github/workflows/manual-deploy.yaml
==================================================
name: Manual-CICD

on:
  workflow_dispatch:
    inputs:
      environments:
        description: 'Which environments to release to'
        required: true
        type: choice
        options:
          - '["integration", "staging", "customer-sandbox-1", "production"]'
          - '["staging", "customer-sandbox-1", "production"]'
          - '["customer-sandbox-1", "production"]'
          - '["production"]'
      hotfix-tag:
        description: 'Mark if you are releasing a hotfix'
        required: false
        type: boolean

jobs:
  Tests:
    uses: ./.github/workflows/run-tests.yaml
    secrets: inherit
  CICD:
    uses: papayaglobal/workflows/.github/workflows/manual-deploy.yaml@main
    needs: Tests
    with:
      service-name: file-generator-engine
      java-ver: 17
      distribution: 'temurin'
      docker-context: ./
      dockerfile-path: ./Dockerfile
      runners: payroll
      account: core
      environments: ${{ inputs.environments }}
      hotfix-tag: ${{ inputs.hotfix-tag }}
    secrets: inherit
    

==================================================
File: file-generator-engine/.github/workflows/deploy.yaml
==================================================
name: CICD

on:
  pull_request_target:
    types: [closed]
    branches:
      - main
    paths-ignore:
      - '**.md'
      - '**/*.md'
      - '**/.gitignore'
      - '.gitignore'
      - '**/CODEOWNERS'
      - 'CODEOWNERS'
      - '**/.dockerignore'
      - '.dockerignore'

jobs:
  CICD:
    uses: papayaglobal/workflows/.github/workflows/deploy.yaml@main
    with:
      service-name: file-generator-engine
      java-ver: 17
      distribution: 'temurin'
      docker-context: ./
      dockerfile-path: ./Dockerfile
      runners: payroll
      account: core
    secrets: inherit


==================================================
File: file-generator-engine/.github/README.md
==================================================
# Github Workflows

## Branching Strategy

Branching model is [Scaled Trunk-Based Development](https://trunkbaseddevelopment.com/#scaled-trunk-based-development).

![Branching and release model](https://github.com/papayaglobal/workflows/blob/main/.github/branching-and-release-model.png)
*Branching model*

There are no restrictions on branch names for integration with Jira to work propery, because [Jira wants branch name to include Jira issue key](https://support.atlassian.com/jira-cloud-administration/docs/integrate-with-development-tools/#How-it-works).

### Development flow for new releases

* Create branch from `main` into a new development branch.
* Push your code.
* (optionally) Use manual deploy workflow to deploy intermediate result to integration.
* Create a PR to `main`.
* Rebase from main if needed.
* Merge after requirments are met (PR is approved and CI/CD checks are a success).
* Wait till CI/CD creates new release and deploys it to integration automatically.
* Review deployment to integration.
* (optional) if everything's fine, go to GitHub Actions and approve deployments to staging.
* (optional) if everything's fine, go to GitHub Actions and approve deployments to production.

### Development flow for hotfixes

Hotfix (option 1):

* Create branch from latest version tag deployed to production into new hotfix branch
* Push your code.
* Use manual deploy workflow to deploy result to integration / staging / production from the hotfix branch.
* Rebase from main.
* Merge after requirments are met (PR is approved and CI/CD checks are a success).

Hotfix (option 2):

* Push fix to `main`.
* Create branch from latest version tag deployed to production into new hotfix branch.
* Cherry pick hotfix commit from `main` to hotfix branch.
* Use manual deploy workflow to deploy result to integration / staging / production from the hotfix branch.
* Hotfix branch doesn't need to be merged as the code is already up to date in `main`.

## Versioning

Product versions is based on [calver](https://calver.org/).

There should be a git tag for each released version.

Versions for new release (and hotfix) is calculated automatically, see [CI/CD Pipelines](#cicd-pipelines).

## CI/CD Pipelines

We use [GitHub Actions](https://docs.github.com/en/actions) workflows for CI/CD pipelines.

![GitHub Actions Worflow](https://github.com/papayaglobal/workflows/blob/main/.github/cicd-diagram.png)
*GitHub Actions Worflow*

Workflows are trigged by different events: pushing into head branch of PR to main, PR merge into main and manual trigger.

[Tests workflow](/.github/workflows/run-tests.yaml) runs on the last commit in PR branch to `main`.

[Deploy workflow](/.github/workflows/deploy.yaml) runs when PR is merged to `main`. It calculates new version, builds and pushes image to ECR, pushes version tag to main. Then it initiates deployment jobs to all environments.

[Manual deploy workflow](/.github/workflows/manual-deploy.yaml) is triggered manually from GitHub Actions UI. It builds and pushes image to ECR and Then it initiates deployment jobs to chosen environments. Useful when you want to test your code from PR before merge or when need to release a hotfix.

## GitHub Repository Settings

Default branch: `main`.

### Pull Requests Settings

* Allow merge commits.
* Allow squash merging.
* Allow rebase merging.
* Updating pull request branches is enforced.
* Allow auto-merge.

### Branch Protection Rules for `main`

* Require a pull request before merging.
* Require approvals.
* Dismiss stale pull request approvals when new commits are pushed.
* Require status checks to pass before merging: `test`.
* Require branches to be up to date before merging.
* Require conversation resolution before merging.

### Environments protection rules

Integration: no approvers required.

Staging: requires approval from stg-approvers that are set for this repo specifically thorugh payments-infrastructure repository.

Production: requires approval from prod-approvers that are set for this repo specifically thorugh payments-infrastructure repository.

### Interested in adding more of your services to the new CI/CD?

Follow the following guide: https://papayaglobal.atlassian.net/wiki/spaces/PR/pages/2671968268/How+to+self+onboard+to+the+new+CI+CD+process.


==================================================
File: file-generator-engine/.github/cicd-doc.md
==================================================
# Github Workflows

## Branching Strategy

Branching model is [Scaled Trunk-Based Development](https://trunkbaseddevelopment.com/#scaled-trunk-based-development).

![Branching and release model](https://github.com/papayaglobal/workflows/blob/main/.github/branching-and-release-model.png)
*Branching model*

There are no restrictions on branch names for integration with Jira to work propery, because [Jira wants branch name to include Jira issue key](https://support.atlassian.com/jira-cloud-administration/docs/integrate-with-development-tools/#How-it-works).

### Development flow for new releases

* Create branch from `main` into a new development branch.
* Push your code.
* (optionally) Use manual deploy workflow to deploy intermediate result to integration.
* Create a PR to `main`.
* Rebase from main if needed.
* Merge after requirments are met (PR is approved and CI/CD checks are a success).
* Wait till CI/CD creates new release and deploys it to integration automatically.
* Review deployment to integration.
* (optional) if everything's fine, go to GitHub Actions and approve deployments to staging.
* (optional) if everything's fine, go to GitHub Actions and approve deployments to demo.
* (optional) if everything's fine, go to GitHub Actions and approve deployments to production.

### Development flow for hotfixes

Hotfix (option 1):

* Create branch from latest version tag deployed to production into new hotfix branch
* Push your code.
* Use manual deploy workflow to deploy result to integration / staging / production / demo from the hotfix branch.
* Rebase from main.
* Merge after requirments are met (PR is approved and CI/CD checks are a success).

Hotfix (option 2):

* Push fix to `main`.
* Create branch from latest version tag deployed to production into new hotfix branch.
* Cherry pick hotfix commit from `main` to hotfix branch.
* Use manual deploy workflow to deploy result to integration / staging / production / demo from the hotfix branch.
* Hotfix branch doesn't need to be merged as the code is already up to date in `main`.

## Versioning

Product versions is based on [calver](https://calver.org/).

There is an option to override and use [semver](https://papayaglobal.atlassian.net/wiki/spaces/DOPS/pages/2774368279/Using+semver+instead+of+calver+in+CI+CD)

There should be a git tag for each released version.

Versions for new release (and hotfix) is calculated automatically, see [CI/CD Pipelines](#cicd-pipelines).

## CI/CD Pipelines

We use [GitHub Actions](https://docs.github.com/en/actions) workflows for CI/CD pipelines.

![GitHub Actions Worflow](https://github.com/papayaglobal/workflows/blob/main/.github/cicd-diagram.png)
*GitHub Actions Worflow*

Workflows are trigged by different events: pushing into head branch of PR to main, PR merge into main and manual trigger.

[Tests workflow](/.github/workflows/run-tests.yaml) runs on the last commit in PR branch to `main`.

[Deploy workflow](/.github/workflows/deploy.yaml) runs when PR is merged to `main`. It calculates new version, builds and pushes image to ECR, pushes version tag to main. Then it initiates deployment jobs to all environments.

[Manual deploy workflow](/.github/workflows/manual-deploy.yaml) is triggered manually from GitHub Actions UI. It builds and pushes image to ECR and Then it initiates deployment jobs to chosen environments. Useful when you want to test your code from PR before merge or when need to release a hotfix.

## GitHub Repository Settings

Default branch: `main`.

### Pull Requests Settings

* Allow merge commits.
* Allow squash merging.
* Allow rebase merging.
* Updating pull request branches is enforced.
* Allow auto-merge.
* Require Branch and PR name to include Jira issue ID.

### Branch Protection Rules for `main`

* Require a pull request before merging.
* Require approvals.
* Dismiss stale pull request approvals when new commits are pushed.
* Require status checks to pass before merging: `test`.
* Require branches to be up to date before merging.
* Require conversation resolution before merging.

### Environments protection rules

Integration: no approvers required.

Staging: requires approval from stg-approvers that are set for this repo specifically through cloud-infra repository.

Production: requires approval from prod-approvers that are set for this repo specifically through cloud-infra repository.

### Interested in adding more of your services to the new CI/CD?

Follow the following guide: https://papayaglobal.atlassian.net/wiki/spaces/PR/pages/2671968268/How+to+self+onboard+to+the+new+CI+CD+process.


==================================================
File: file-generator-engine/docker-compose.yml
==================================================
version: '1'
services:
  rabbitmq:
    image: rabbitmq:3-management
    container_name: rabbitmq
    hostname: rabbitmq
    ports:
      - "15672:15672"
      - "5672:5672"
    healthcheck:
      test: [ "CMD-SHELL", "rabbitmqctl status" ]
      interval: 10s
      timeout: 5s
      retries: 5

  rabbitmq-migration:
    image: 171243386177.dkr.ecr.eu-west-1.amazonaws.com/papaya-mq-migration:integration
    environment:
      PY_RABBIT_MGMT_BASE_URL: http://rabbitmq:15672
      PY_RABBIT_CONN_STRING: amqp://guest:guest@rabbitmq:5672
      PY_RABBIT_MGMT_USER: guest
      PY_RABBIT_MGMT_PASSWORD: guest
      PY_LOCAL_PARAM_STORE: true
    depends_on:
      rabbitmq:
        condition: service_healthy
  file-generator-engine:
    image: file-generator-engine:local
    build:
      context: .
      dockerfile: ./Dockerfile
    restart: always
    depends_on: [ rabbitmq,rabbitmq-migration ]
    ports: [ '8120:8120' ]
    environment:
      RABBITMQ_URL: "amqp://guest:guest@rabbitmq:5672/papaya"
      SPRING_PROFILES_ACTIVE: "local"
      LOG_LEVEL: "debug"
      AWS_ACCESS_KEY_ID: test
      AWS_SECRET_ACCESS_KEY: test
      AWS_REGION: us-east-1
      S3_ENDPOINT: http://localstack:4566
      AMAZON_ORG_BUCKET_NAME: test
      JWT_SIGNING_KEY: 12453
    healthcheck:
      test: [ "CMD", "curl", "-f", "http://localhost:8120/file-generator-engine/actuator/health" ]



==================================================
File: file-generator-engine/compose-dev.yaml
==================================================
services:
  app:
    entrypoint:
    - sleep
    - infinity
    image: docker/dev-environments-java:stable-1
    init: true
    volumes:
    - type: bind
      source: /var/run/docker.sock
      target: /var/run/docker.sock



==================================================
File: file-generator-engine/src/test/java/com/papaya/file_generator/engine/configuration/FileGeneratorHandlerConfigurationTest.java
==================================================
package com.papaya.file_generator.engine.configuration;

import org.junit.jupiter.api.DisplayName;
import org.junit.jupiter.api.Test;
import org.mockito.Mockito;
import org.springframework.core.io.Resource;
import org.springframework.core.io.ResourceLoader;

import java.io.IOException;
import java.io.InputStream;

import static org.junit.jupiter.api.Assertions.assertThrows;
import static org.mockito.Mockito.when;

class FileGeneratorHandlerConfigurationTest {


    @Test
    @DisplayName("Test no handlers configured")
    void strategyMap() throws IOException {
        ResourceLoader resourceLoader = Mockito.mock(ResourceLoader.class);
        Resource resource = Mockito.mock(Resource.class);

        when(resourceLoader.getResource("classpath:handlers.properties")).thenReturn(resource);
        when(resource.getInputStream()).thenReturn(InputStream.nullInputStream());

        FileGeneratorHandlerConfiguration configuration = new FileGeneratorHandlerConfiguration(resourceLoader);

        assertThrows(RuntimeException.class, configuration::strategyMap, "No handlers configured");
    }
}


==================================================
File: file-generator-engine/src/test/java/com/papaya/file_generator/engine/service/FileGeneratorServiceTest.java
==================================================
package com.papaya.file_generator.engine.service;
import com.papaya.file_generator.commons.handler.FileGeneratorHandler;
import org.junit.jupiter.api.DisplayName;
import org.junit.jupiter.api.Test;

import java.util.HashMap;
import java.util.Map;

import static org.junit.jupiter.api.Assertions.assertThrows;

class FileGeneratorServiceTest {
    private FileGeneratorService service;

    @Test
    @DisplayName("Test no valid handler")
    void handlerMap() {
        Map<String, FileGeneratorHandler> handlerMap = new HashMap<>();

        service = new FileGeneratorService(handlerMap);
        HashMap<String, Object> parameters = new HashMap<>();
        String handlerName = "handlerName";

        assertThrows(IllegalArgumentException.class, () ->
                service.generate(handlerName, parameters)
        ,"No class handler was found for: handlerName");

    }

}


==================================================
File: file-generator-engine/src/test/java/com/papaya/file_generator/handlers/template_based_excel/TemplateBasedExcelHandlerTest.java
==================================================
package com.papaya.file_generator.handlers.template_based_excel;

import com.papaya.file_generator.commons.handler.GenerateCommandResponseDTO;
import com.papaya.file_generator.commons.util.AwsClient;
import com.papaya.file_generator.handlers.template_based_excel.model.ExcelCellDTO;
import com.papaya.file_generator.handlers.template_based_excel.model.ExcelCellFormattedValueDTO;
import com.papaya.file_generator.handlers.template_based_excel.model.ExcelFileDTO;
import com.papaya.file_generator.handlers.template_based_excel.model.ExcelSheetDTO;
import org.junit.jupiter.api.Assertions;
import org.junit.jupiter.api.DisplayName;
import org.junit.jupiter.api.Test;
import org.mockito.MockedConstruction;
import org.mockito.Mockito;

import java.io.FileInputStream;
import java.io.FileNotFoundException;
import java.util.LinkedHashMap;
import java.util.Map;
import java.util.TreeMap;

import static org.junit.Assert.assertThrows;
import static org.mockito.ArgumentMatchers.anyString;
import static org.mockito.Mockito.*;


class TemplateBasedExcelHandlerTest {

    public static final int FILE_EXPIRATION_TIME = 1000;

    TemplateBasedExcelHandler spyTemplateBasedExcelHandler;
    AwsClient mockAwsClient;



    @Test
    @DisplayName("Test E2E using a valid file")
    void generateFileLocal() throws Exception {

        LinkedHashMap<String, Object> parameters = new LinkedHashMap<>();

        parameters.put("templateUrl", "src/test/resources/salary_update_template.xlsx");
        parameters.put("newFileName", "test1.xlsx");
        parameters.put("dataUrl", "src/test/resources/testData.json");


        String uploadFolder = "dev/file-generator/";
        String bucketName = "papaya-data-files";
        String awsRegion = "eu-west-1";
        int fileExpirationTime = 1000;

        try (MockedConstruction<AwsClient> mockedConstruction = Mockito.mockConstruction(AwsClient.class, (mock, context) -> {
            mockAwsClient = mock;
            when(mock.getPresignedUrl(anyString(), anyInt())).thenReturn("mocked-url");
            doNothing().when(mock)
                       .copyPresignedFile(anyString(), anyString());
            doNothing().when(mock).persistData(anyString(), anyString());
            when(mock.readPresignedFileAsStream(anyString())).thenAnswer(invocation -> {
                String filePath = invocation.getArgument(0);
                return new FileInputStream(filePath);
            });
        })) {
            spyTemplateBasedExcelHandler = spy(new TemplateBasedExcelHandler(mockAwsClient));
            doReturn("mocked-extractedFile").when(spyTemplateBasedExcelHandler)
                                            .extractFileNameFromPresignedUrl(anyString());
            GenerateCommandResponseDTO fileURL = spyTemplateBasedExcelHandler.generateFileWithCustomRowCount(bucketName, uploadFolder, awsRegion, fileExpirationTime, parameters, 200);
            Assertions.assertEquals("mocked-url", fileURL.getUrl());
        }


    }

    @Test
    @DisplayName("Test E2E without parameters")
    void generateFileWithoutParameters() {
        try (MockedConstruction<AwsClient> mockedConstruction = Mockito.mockConstruction(AwsClient.class, (mock, context) -> {
            mockAwsClient = mock;
            when(mock.getPresignedUrl(anyString(), anyInt())).thenReturn("mocked-url");
            doNothing().when(mock)
                       .copyPresignedFile(anyString(), anyString());
            doNothing().when(mock).persistData(anyString(), anyString());
            when(mock.readPresignedFileAsStream(anyString())).thenAnswer(invocation -> {
                String filePath = invocation.getArgument(0);
                return new FileInputStream(filePath);
            });
        })) {
            spyTemplateBasedExcelHandler = spy(new TemplateBasedExcelHandler(mockAwsClient));
            doReturn("mocked-extractedFile").when(spyTemplateBasedExcelHandler)
                                            .extractFileNameFromPresignedUrl(anyString());
            assertThrowsException(null, "src/test/resources/testData.json", "dev/file-generator/", "papaya-data-files", "eu-west-1", IllegalArgumentException.class, "Template URL is required");
        }
    }

    @Test
    @DisplayName("Test E2E with empty bucketName")
    void generateFileWithEmptyBucketName() {
        try (MockedConstruction<AwsClient> mockedConstruction = Mockito.mockConstruction(AwsClient.class, (mock, context) -> {
            mockAwsClient = mock;
            when(mock.getPresignedUrl(anyString(), anyInt())).thenReturn("mocked-url");
            doNothing().when(mock)
                       .copyPresignedFile(anyString(), anyString());
            doNothing().when(mock).persistData(anyString(), anyString());
            when(mock.readPresignedFileAsStream(anyString())).thenAnswer(invocation -> {
                String filePath = invocation.getArgument(0);
                return new FileInputStream(filePath);
            });
        })) {
            spyTemplateBasedExcelHandler = spy(new TemplateBasedExcelHandler(mockAwsClient));
            doReturn("mocked-extractedFile").when(spyTemplateBasedExcelHandler)
                                            .extractFileNameFromPresignedUrl(anyString());
            assertThrowsException("src/test/resources/salary_update_template.xlsx", "src/test/resources/testData.json", "dev/file-generator/", "", "eu-west-1", IllegalArgumentException.class, "Bucket name is required");
        }
    }

    @Test
    @DisplayName("Test E2E with empty uploadFolder")
    void generateFileWithEmptyUploadFolder() {
        try (MockedConstruction<AwsClient> mockedConstruction = Mockito.mockConstruction(AwsClient.class, (mock, context) -> {
            mockAwsClient = mock;
            when(mock.getPresignedUrl(anyString(), anyInt())).thenReturn("mocked-url");
            doNothing().when(mock)
                       .copyPresignedFile(anyString(), anyString());
            doNothing().when(mock).persistData(anyString(), anyString());
            when(mock.readPresignedFileAsStream(anyString())).thenAnswer(invocation -> {
                String filePath = invocation.getArgument(0);
                return new FileInputStream(filePath);
            });
        })) {
            spyTemplateBasedExcelHandler = spy(new TemplateBasedExcelHandler(mockAwsClient));
            doReturn("mocked-extractedFile").when(spyTemplateBasedExcelHandler)
                                            .extractFileNameFromPresignedUrl(anyString());
            assertThrowsException("src/test/resources/salary_update_template.xlsx", "src/test/resources/testData.json", "", "papaya-data-files", "eu-west-1", IllegalArgumentException.class, "Upload folder is required");
        }
    }

    //create test with no awsRegion
    @Test
    @DisplayName("Test E2E with no awsRegion")
    void generateFileWithNoAwsRegion() {
        try (MockedConstruction<AwsClient> mockedConstruction = Mockito.mockConstruction(AwsClient.class, (mock, context) -> {
            mockAwsClient = mock;
            when(mock.getPresignedUrl(anyString(), anyInt())).thenReturn("mocked-url");
            doNothing().when(mock)
                       .copyPresignedFile(anyString(), anyString());
            doNothing().when(mock).persistData(anyString(), anyString());
            when(mock.readPresignedFileAsStream(anyString())).thenAnswer(invocation -> {
                String filePath = invocation.getArgument(0);
                return new FileInputStream(filePath);
            });
        })) {
            spyTemplateBasedExcelHandler = spy(new TemplateBasedExcelHandler(mockAwsClient));
            doReturn("mocked-extractedFile").when(spyTemplateBasedExcelHandler)
                                            .extractFileNameFromPresignedUrl(anyString());
            assertThrowsException("src/test/resources/salary_update_template.xlsx", "src/test/resources/testData.json", "dev/file-generator/", "papaya-data-files", "", IllegalArgumentException.class, "AWS region is required");
        }
    }

    //create test with non-valid templateUrl file
    @Test
    @DisplayName("Test E2E with non valid templateUrl file")
    void generateFileWithNonValidTemplateUrl() {
        try (MockedConstruction<AwsClient> mockedConstruction = Mockito.mockConstruction(AwsClient.class, (mock, context) -> {
            mockAwsClient = mock;
            when(mock.getPresignedUrl(anyString(), anyInt())).thenReturn("mocked-url");
            doNothing().when(mock)
                       .copyPresignedFile(anyString(), anyString());
            doNothing().when(mock).persistData(anyString(), anyString());
            when(mock.readPresignedFileAsStream(anyString())).thenAnswer(invocation -> {
                String filePath = invocation.getArgument(0);
                return new FileInputStream(filePath);
            });
        })) {
            spyTemplateBasedExcelHandler = spy(new TemplateBasedExcelHandler(mockAwsClient));
            doReturn("mocked-extractedFile").when(spyTemplateBasedExcelHandler)
                                            .extractFileNameFromPresignedUrl(anyString());
            assertThrowsException("src/test/resources/salary_update_template1.xlsx", "src/test/resources/testData.json", "dev/file-generator/", "papaya-data-files", "eu-west-1", FileNotFoundException.class, "");
        }
    }

    //create test with non-valid dataUrl file
    @Test
    @DisplayName("Test E2E with non valid dataUrl file")
    void generateFileWithNonValidDataUrl() {
        assertThrowsException("src/test/resources/salary_update_template.xlsx", "src/test/resources/testData11.json", "dev/file-generator/", "papaya-data-files", "eu-west-1", RuntimeException.class, "");
    }

    //create test with json file as excel template
    @Test
    @DisplayName("Test E2E with json file as excel template")
    void generateFileWithJsonTemplateUrl() {
        try (MockedConstruction<AwsClient> mockedConstruction = Mockito.mockConstruction(AwsClient.class, (mock, context) -> {
            mockAwsClient = mock;
            when(mock.getPresignedUrl(anyString(), anyInt())).thenReturn("mocked-url");
            doNothing().when(mock)
                       .copyPresignedFile(anyString(), anyString());
            doNothing().when(mock).persistData(anyString(), anyString());
            when(mock.readPresignedFileAsStream(anyString())).thenAnswer(invocation -> {
                String filePath = invocation.getArgument(0);
                return new FileInputStream(filePath);
            });
        })) {
            spyTemplateBasedExcelHandler = spy(new TemplateBasedExcelHandler(mockAwsClient));
            doReturn("mocked-extractedFile").when(spyTemplateBasedExcelHandler)
                                            .extractFileNameFromPresignedUrl(anyString());
            assertThrowsException("src/test/resources/testData.json", "src/test/resources/testData.json", "dev/file-generator/", "papaya-data-files", "eu-west-1", IllegalArgumentException.class, "");
        }
    }

    //create test with excelTemplate file as json
    @Test
    @DisplayName("Test E2E with excelTemplate file as json")
    void generateFileWithExcelTemplateUrlAsJson() {
        assertThrowsException("src/test/resources/salary_update_template.xlsx", "src/test/resources/salary_update_template.xlsx", "dev/file-generator/", "papaya-data-files", "eu-west-1", RuntimeException.class, "Failed to parse the response");
    }


    //create test that generates an empty Excel file and uses it as templateUrl
    @Test
    @DisplayName("Test E2E with empty excel file as templateUrl")
    void generateFileWithEmptyExcelTemplateUrl() throws Exception {

        LinkedHashMap<String, Object> parameters = new LinkedHashMap<>();

        parameters.put("templateUrl", "src/test/resources/empty_template.xlsx");
        parameters.put("newFileName", "test1.xlsx");
        parameters.put("dataUrl", "src/test/resources/testData.json");

        String uploadFolder = "dev/file-generator/";
        String bucketName = "papaya-data-files";
        String awsRegion = "eu-west-1";
        try (MockedConstruction<AwsClient> mockedConstruction = Mockito.mockConstruction(AwsClient.class, (mock, context) -> {
            mockAwsClient = mock;
            when(mock.getPresignedUrl(anyString(), anyInt())).thenReturn("mocked-url");
            doNothing().when(mock)
                       .copyPresignedFile(anyString(), anyString());
            doNothing().when(mock).persistData(anyString(), anyString());
            when(mock.readPresignedFileAsStream(anyString())).thenAnswer(invocation -> {
                String filePath = invocation.getArgument(0);
                return new FileInputStream(filePath);
            });
        })) {
            spyTemplateBasedExcelHandler = spy(new TemplateBasedExcelHandler(mockAwsClient));
            doReturn("mocked-extractedFile").when(spyTemplateBasedExcelHandler)
                                            .extractFileNameFromPresignedUrl(anyString());
            GenerateCommandResponseDTO fileURL = spyTemplateBasedExcelHandler.generateFileWithCustomRowCount(bucketName, uploadFolder, awsRegion, FILE_EXPIRATION_TIME, parameters, 200);
            Assertions.assertEquals("mocked-url", fileURL.getUrl());
        }


    }

    //create test with an empty json file
    @Test
    @DisplayName("Test E2E with empty json file")
    void generateFileWithEmptyJsonDataUrl() {
        assertThrowsException("src/test/resources/emptyJson.json", "src/test/resources/salary_update_template.xlsx", "dev/file-generator/", "papaya-data-files", "eu-west-1", RuntimeException.class, "Failed to parse the json Data");
    }

    //create test with a corrupted json file and expect runtime exception
    @Test
    @DisplayName("Test E2E with corrupted json file")
    void generateFileWithCorruptedJsonDataUrl() {
        assertThrowsException("src/test/resources/corruptedFile.json", "src/test/resources/salary_update_template.xlsx", "dev/file-generator/", "papaya-data-files", "eu-west-1", RuntimeException.class, "Failed to parse the json Data");
    }

    private void assertThrowsException(String dataUrl, String templateUrl, String uploadFolder, String bucketName, String awsRegion, Class<? extends Exception> expectedThrowable, String exceptionMessage) {
        LinkedHashMap<String, Object> parameters = new LinkedHashMap<>();

        parameters.put("templateUrl", templateUrl);
        parameters.put("newFileName", "test1.xlsx");
        parameters.put("dataUrl", dataUrl);

        assertThrows(exceptionMessage, expectedThrowable, () -> spyTemplateBasedExcelHandler.generateFileWithCustomRowCount(bucketName, uploadFolder, awsRegion, TemplateBasedExcelHandlerTest.FILE_EXPIRATION_TIME, parameters, 200));
    }

    @Test
    @DisplayName("Test with multiple sheets and bigger tables")
    void generateFileWithMultipleSheets() throws Exception {
        ExcelFileDTO excelFile = new ExcelFileDTO();
        ExcelSheetDTO salaryUpdateSheet = new ExcelSheetDTO();
        salaryUpdateSheet.setSheetName("Salary Updates");

        Map<String, ExcelCellDTO> salaryUpdateData = new TreeMap<>();

        salaryUpdateData.put("title", new ExcelCellFormattedValueDTO("Salary Update").setBold());
        salaryUpdateData.put("subtitle", new ExcelCellFormattedValueDTO("01–31 Mar 2022"));
        salaryUpdateData.put("lastupdate", new ExcelCellFormattedValueDTO("Last updated by Finance Controller at 26 Apr 2022 14:48:23 GMT"));
        salaryUpdateData.put("comments", new ExcelCellFormattedValueDTO("No comments."));

        salaryUpdateData.put("body", JsonGenerator.generateTableValues(1000));
        salaryUpdateData.put("body2", JsonGenerator.generateTableValues(1000));

        salaryUpdateSheet.setSheetData(salaryUpdateData);
        excelFile.addSheet(salaryUpdateSheet);

        ExcelSheetDTO expenseReport = new ExcelSheetDTO();
        expenseReport.setSheetName("Expenses Reports");
        Map<String, ExcelCellDTO> expenseReportData = new TreeMap<>();
        expenseReportData.put("body", JsonGenerator.generateTableValues(1000));
        expenseReport.setSheetData(expenseReportData);
        excelFile.addSheet(expenseReport);

        ExcelSheetDTO pto = new ExcelSheetDTO();
        pto.setSheetName("PTO");
        Map<String, ExcelCellDTO> ptoData = new TreeMap<>();
        ptoData.put("comments", new ExcelCellFormattedValueDTO("Gross Reported days/hours shall be calculated based on the local regulation and applied policy"));
        ptoData.put("body", JsonGenerator.generateTableValues(1000));
        pto.setSheetData(ptoData);
        excelFile.addSheet(pto);

        ExcelSheetDTO accountingCodes = new ExcelSheetDTO();
        accountingCodes.setSheetName("Accounting codes list");
        Map<String, ExcelCellDTO> accountingCodesData = new TreeMap<>();
        accountingCodesData.put("body", JsonGenerator.generateTableValues(1000));
        accountingCodes.setSheetData(accountingCodesData);
        excelFile.addSheet(accountingCodes);

        ExcelSheetDTO differences = new ExcelSheetDTO();
        differences.setSheetName("Differences");
        Map<String, ExcelCellDTO> differencesData = new TreeMap<>();
        differencesData.put("body1", JsonGenerator.generateTableValues(1000));
        differencesData.put("body2", JsonGenerator.generateTableValues(2));
        differencesData.put("body3", JsonGenerator.generateTableValues(1000));
        differences.setSheetData(differencesData);
        excelFile.addSheet(differences);


        String jsonPath = "src/test/resources/testData2.json";
        JsonGenerator.save(excelFile, jsonPath);


        LinkedHashMap<String, Object> parameters = new LinkedHashMap<>();

        parameters.put("templateUrl", "src/test/resources/salary_update_template.xlsx");
        parameters.put("newFileName", "src/test/resources/test1.xlsx");
        parameters.put("dataUrl", jsonPath);

        String uploadFolder = "dev/file-generator/";
        String bucketName = "papaya-data-files";
        String awsRegion = "eu-west-1";

        try (MockedConstruction<AwsClient> mockedConstruction = Mockito.mockConstruction(AwsClient.class, (mock, context) -> {
            mockAwsClient = mock;
            when(mock.getPresignedUrl(anyString(), anyInt())).thenReturn("mocked-url");
            doNothing().when(mock)
                       .copyPresignedFile(anyString(), anyString());
            doNothing().when(mock).persistData(anyString(), anyString());
            when(mock.readPresignedFileAsStream(anyString())).thenAnswer(invocation -> {
                String filePath = invocation.getArgument(0);
                return new FileInputStream(filePath);
            });
        })) {
            spyTemplateBasedExcelHandler = spy(new TemplateBasedExcelHandler(mockAwsClient));
            doReturn("mocked-extractedFile").when(spyTemplateBasedExcelHandler)
                                            .extractFileNameFromPresignedUrl(anyString());
            GenerateCommandResponseDTO fileURL = spyTemplateBasedExcelHandler.generateFileWithCustomRowCount(bucketName, uploadFolder, awsRegion, FILE_EXPIRATION_TIME, parameters, 200);
            Assertions.assertEquals("mocked-url", fileURL.getUrl());
        }


    }
}



==================================================
File: file-generator-engine/src/test/java/com/papaya/file_generator/handlers/template_based_excel/JsonGenerator.java
==================================================
package com.papaya.file_generator.handlers.template_based_excel;

import com.fasterxml.jackson.databind.ObjectMapper;
import com.papaya.file_generator.handlers.template_based_excel.model.ExcelCellDTO;
import com.papaya.file_generator.handlers.template_based_excel.model.ExcelCellFormattedValueDTO;
import com.papaya.file_generator.handlers.template_based_excel.model.ExcelCellTableValueDTO;
import com.papaya.file_generator.handlers.template_based_excel.model.ExcelFileDTO;

import java.io.File;
import java.io.IOException;
import java.util.ArrayList;
import java.util.List;
import java.util.Random;

public class JsonGenerator {
    public static void save(ExcelFileDTO excelFile, String path) {
        ObjectMapper mapper = new ObjectMapper();

        try {
            mapper.writeValue(new File(path), excelFile);
        } catch (IOException e) {
            throw new RuntimeException(e);
        }
    }

    public static ExcelCellTableValueDTO generateTableValues(int numRows) {
        String[] columnNames = {
                "Contract id", "Employee Number", "Worker Name", "Hire Date", "Termination Date",
                "Cost Center", "Salary", "Seniority Allowance", "Health Allowance", "Car Allowance",
                "Overtime Pay - Taxed", "Weekday Early Shift Allowance", "House Allowance",
                "Meals Allowance", "Overtime", "Bonus", "Commission", "Birthday Voucher/Gift Gross",
                "Wedding Allowance Gross", "EE - Dorm Deduction", "EE - Phone Deduction", "Meals",
                "Commission/Bonus", "Backdated Pay", "Travel Allowance", "Maternity Pay Reimb",
                "Phone/Internet Allowance", "Christmas Bonus", "Private Savings", "Unused Holiday",
                "Transportation Reimb", "Expense Reimb", "Comment", "System Comment", "Updated By"
        };

        ExcelCellTableValueDTO tableValues = new ExcelCellTableValueDTO();

        List<ExcelCellDTO> tableRow = new ArrayList<>();
        for (String columnName : columnNames) {
            tableRow.add(new ExcelCellFormattedValueDTO(columnName).setBold());
        }

        tableValues.addRow(tableRow);

        for (int i = 0; i < numRows; i++) {
            tableValues.addRow(generateRandomData(columnNames));
        }
        return tableValues;
    }

    public static List<ExcelCellDTO> generateRandomData(String[] columnNames) {
        Random random = new Random();


        List<ExcelCellDTO> tableRow = new ArrayList<>();
        for (String columnName : columnNames) {
            tableRow.add(new ExcelCellFormattedValueDTO(generateRandomValue(columnName, random)));
        }
        return tableRow;
    }

    public static String generateRandomValue(String columnName, Random random) {
        StringBuilder word = new StringBuilder();
        for (int i = 0; i < 10; i++) {
            char c = (char) (random.nextInt(26) + 'a');
            word.append(c);
        }
        return word.toString();

    }
}


==================================================
File: file-generator-engine/src/main/resources/application-local.properties
==================================================
logging.level.web=info
logging.config=classpath:logback-spring.xml

server.port=8120
server.servlet.context-path=/file-generator-engine

rabbitmq.url=amqp://localhost/papaya
rabbitmq.enabled=true
rabbitmq.exchange=file_generator.tx
rabbitmq.queue=file-generator.q

amazon.bucket.name=papaya-file-generator-integration
amazon.region.name=eu-west-1
amazon.file.expiration.time=86400000
amazon.folder.name=generated-files/

management.endpoints.web.exposure.include=health
xml.file.max.row.count=201



==================================================
File: file-generator-engine/src/main/resources/handlers.properties
==================================================
handler.excel-template=com.papaya.file_generator.handlers.template_based_excel.TemplateBasedExcelHandler
handler.template=com.papaya.file_generator.handlers.template_based_excel.TemplateBasedExcelHandler


==================================================
File: file-generator-engine/src/main/resources/application.properties
==================================================
logging.level.web=info
logging.config=classpath:logback-spring.xml

server.port=8120
server.servlet.context-path=/file-generator-engine

rabbitmq.enabled=true
rabbitmq.exchange=file_generator.tx
rabbitmq.queue=file-generator.q


amazon.region.name=eu-west-1

management.endpoints.web.exposure.include=health
management.endpoint.metrics.enabled=true


management.statsd.metrics.export.enabled=true
management.statsd.metrics.export.port=8125
management.metrics.tags.service="file-generator-engine"
xml.file.max.row.count=201



==================================================
File: file-generator-engine/src/main/java/com/papaya/file_generator/engine/configuration/FileGeneratorHandlerConfiguration.java
==================================================
package com.papaya.file_generator.engine.configuration;

import com.papaya.file_generator.commons.handler.FileGeneratorHandler;
import lombok.AllArgsConstructor;
import lombok.extern.slf4j.Slf4j;
import org.springframework.context.annotation.Bean;
import org.springframework.context.annotation.Configuration;
import org.springframework.core.io.Resource;
import org.springframework.core.io.ResourceLoader;

import java.io.IOException;
import java.io.InputStream;
import java.lang.reflect.InvocationTargetException;
import java.util.HashMap;
import java.util.Map;
import java.util.Properties;

@Configuration
@Slf4j
@AllArgsConstructor
public class FileGeneratorHandlerConfiguration {
    private ResourceLoader resourceLoader;

    @Bean
    public Map<String, FileGeneratorHandler> strategyMap() throws IOException, ClassNotFoundException, InstantiationException, IllegalAccessException, NoSuchMethodException, InvocationTargetException {

        Map<String, FileGeneratorHandler> handlerMap = new HashMap<>();
        Properties properties = new Properties();
        Resource resource = resourceLoader.getResource("classpath:handlers.properties");
        try (InputStream inputStream = resource.getInputStream()) {
            properties.load(inputStream);
        }
        if (properties.isEmpty()) {
            throw new RuntimeException("No handlers configured");
        }
        for (String handlerName : properties.stringPropertyNames()) {
            String className = properties.getProperty(handlerName);
            Class<?> strategyClass = Class.forName(className);
            FileGeneratorHandler handler = (FileGeneratorHandler) strategyClass.getDeclaredConstructor().newInstance();
            handlerMap.put(handlerName, handler);
        }

        return handlerMap;
    }
}


==================================================
File: file-generator-engine/src/main/java/com/papaya/file_generator/engine/util/StackTraceConverter.java
==================================================
package com.papaya.file_generator.engine.util;

import java.io.PrintWriter;
import java.io.StringWriter;

public class StackTraceConverter {

    public static String convertToString(Throwable t) {
        StringWriter stringWriter = new StringWriter();
        t.printStackTrace(new PrintWriter(stringWriter));

        return stringWriter.toString();
    }
}


==================================================
File: file-generator-engine/src/main/java/com/papaya/file_generator/engine/queue/handler/main/FileGeneratorEventHandler.java
==================================================
package com.papaya.file_generator.engine.queue.handler.main;


import com.papaya.amqp.common.AmqpMessage;
import com.papaya.amqp.common.MessageDelivery;
import com.papaya.amqp.common.MessageResponse;
import com.papaya.file_generator.commons.handler.GenerateCommandResponseDTO;
import com.papaya.file_generator.engine.queue.model.GenerateCommandDTO;
import com.papaya.file_generator.engine.service.FileGeneratorService;
import lombok.AllArgsConstructor;
import lombok.extern.slf4j.Slf4j;
import org.springframework.boot.autoconfigure.condition.ConditionalOnProperty;
import org.springframework.stereotype.Controller;

import java.util.Objects;

import static com.papaya.file_generator.engine.queue.handler.main.MessageTypeConstants.HANDLE_GENERATE_COMMAND;


@Slf4j
@Controller
@AllArgsConstructor
@ConditionalOnProperty(prefix = "rabbitmq", name = "enabled")
public class FileGeneratorEventHandler {

    private final FileGeneratorService fileGeneratorService;


    @AmqpMessage(type = HANDLE_GENERATE_COMMAND)
    public MessageResponse onNotificationCommandReceived(GenerateCommandDTO dto, MessageDelivery messageDelivery) {
        log.info("File Generator: Start processing GenerateFileCommand");

        GenerateCommandResponseDTO commandResponseDTO = fileGeneratorService.generate(Objects.requireNonNull(dto.getHandlerName()),
                dto.getParameters());
        log.info("File Generator: Finish processing GenerateFileCommand");

        return new MessageResponse(commandResponseDTO, null);
    }

}


==================================================
File: file-generator-engine/src/main/java/com/papaya/file_generator/engine/queue/handler/main/MessageTypeConstants.java
==================================================
package com.papaya.file_generator.engine.queue.handler.main;

public class MessageTypeConstants {
    public static final String HANDLE_GENERATE_COMMAND = "file-generator.generate.cmd";

}


==================================================
File: file-generator-engine/src/main/java/com/papaya/file_generator/engine/queue/producer/DefaultProducer.java
==================================================
package com.papaya.file_generator.engine.queue.producer;

import com.papaya.amqp.producer.Producer;
import com.papaya.amqp.producer.ProducerOptions;
import com.papaya.file_generator.engine.queue.connection.ProducerConnection;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.boot.autoconfigure.condition.ConditionalOnProperty;
import org.springframework.stereotype.Component;

import javax.annotation.PostConstruct;
import javax.annotation.PreDestroy;

@Component
@ConditionalOnProperty(prefix = "rabbitmq", name = "enabled")
public class DefaultProducer extends Producer {
    @Autowired
    ProducerConnection producerConnection;

    public DefaultProducer() {
        super(ProducerOptions.builder().origin("cycle-manager").build());
    }

    @PostConstruct
    private void postConstruct() throws Exception {
        setConnection(producerConnection);
        init();
    }

    @PreDestroy
    private void preDestroy() {
        try {
            if (isOpened()) {
                close();
            }
        } catch (Exception e) {
            throw new RuntimeException("Failed to close DefaultProducer", e);
        }
    }
}


==================================================
File: file-generator-engine/src/main/java/com/papaya/file_generator/engine/queue/connection/ProducerConnection.java
==================================================
package com.papaya.file_generator.engine.queue.connection;

import com.papaya.amqp.connection.Connection;
import com.papaya.amqp.connection.ConnectionOptions;
import jakarta.annotation.PostConstruct;
import jakarta.annotation.PreDestroy;
import org.springframework.beans.factory.annotation.Value;
import org.springframework.boot.autoconfigure.condition.ConditionalOnProperty;
import org.springframework.stereotype.Component;

@Component
@ConditionalOnProperty(prefix = "rabbitmq", name = "enabled")
public class ProducerConnection extends Connection {
    public ProducerConnection(@Value("${rabbitmq.url}") final String url) throws Exception {
        super(ConnectionOptions.builder().uri(url).build());
    }

    @PostConstruct
    private void postConstruct() throws Exception {
        init();
    }

    @PreDestroy
    private void preDestroy() {
        try {
            close();
        } catch (Exception e) {
            throw new RuntimeException("Failed to close ProducerConnection", e);
        }
    }
}


==================================================
File: file-generator-engine/src/main/java/com/papaya/file_generator/engine/queue/connection/ConsumerConnection.java
==================================================
package com.papaya.file_generator.engine.queue.connection;

import com.papaya.amqp.connection.Connection;
import com.papaya.amqp.connection.ConnectionOptions;
import lombok.extern.slf4j.Slf4j;
import org.springframework.beans.factory.annotation.Value;
import org.springframework.boot.autoconfigure.condition.ConditionalOnProperty;
import org.springframework.stereotype.Component;

import javax.annotation.PostConstruct;
import javax.annotation.PreDestroy;

@Slf4j
@Component
@ConditionalOnProperty(prefix = "rabbitmq", name = "enabled")
public class ConsumerConnection extends Connection {
    public ConsumerConnection(@Value("${rabbitmq.url}") final String url) throws Exception {
        super(ConnectionOptions.builder().uri(url).build());
    }

    @PostConstruct
    private void postConstruct() throws Exception {
        init();
    }

    @PreDestroy
    private void preDestroy() {
        try {
            close();
        } catch (Exception e) {
            throw new RuntimeException("Failed to close ConsumerConnection", e);
        }
    }
}


==================================================
File: file-generator-engine/src/main/java/com/papaya/file_generator/engine/queue/model/GenerateCommandDTO.java
==================================================
package com.papaya.file_generator.engine.queue.model;

import com.papaya.amqp.common.Payload;
import lombok.AllArgsConstructor;
import lombok.NoArgsConstructor;

import java.util.Map;

@AllArgsConstructor
@NoArgsConstructor
public class GenerateCommandDTO extends Payload {
    private String handlerName;
    private Map<String, Object> parameters;

    public String getHandlerName() {
        return handlerName;
    }

    public Map<String, Object> getParameters() {
        return parameters;
    }

    public void setCommand(String handlerName, Map<String, Object> parameters) {
        this.handlerName = handlerName;
        this.parameters = parameters;
    }
}


==================================================
File: file-generator-engine/src/main/java/com/papaya/file_generator/engine/queue/consumer/DefaultConsumer.java
==================================================
package com.papaya.file_generator.engine.queue.consumer;

import com.papaya.amqp.consumer.Consumer;
import com.papaya.amqp.consumer.ConsumerOptions;
import com.papaya.file_generator.engine.queue.connection.ConsumerConnection;
import com.papaya.file_generator.engine.queue.producer.DefaultProducer;
import lombok.extern.slf4j.Slf4j;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.beans.factory.annotation.Value;
import org.springframework.boot.autoconfigure.condition.ConditionalOnProperty;
import org.springframework.context.ApplicationContext;
import org.springframework.stereotype.Service;

import javax.annotation.PostConstruct;
import javax.annotation.PreDestroy;

@Slf4j
@Service
@ConditionalOnProperty(prefix = "rabbitmq", name = "enabled")
public class DefaultConsumer extends Consumer {
    @Autowired
    ConsumerConnection consumerConnection;

    @Autowired
    DefaultProducer defaultProducer;

    DefaultConsumer(@Autowired ApplicationContext applicationContext, @Value("${rabbitmq.exchange}") final String exchange, @Value("${rabbitmq.queue}") final String queue)  {
        super(ConsumerOptions.builder()
                .exchange(exchange)
                .queue(queue)
                .packageName("com.papaya.file_generator.engine.queue.handler.main")
                .locator(applicationContext::getBean).build()
        );
    }

    @PostConstruct
    private void postConstruct() throws Exception {
        setConnection(consumerConnection);
        setProducer(defaultProducer);
        init();
    }

    @PreDestroy
    private void preDestroy() {
        try {
            close();
        } catch (Exception e) {
            throw new RuntimeException("Failed to close DefaultConsumer", e);
        }
    }

}


==================================================
File: file-generator-engine/src/main/java/com/papaya/file_generator/engine/service/FileGeneratorService.java
==================================================
package com.papaya.file_generator.engine.service;

import com.papaya.file_generator.commons.handler.FileGeneratorHandler;
import com.papaya.file_generator.commons.handler.GenerateCommandResponseDTO;
import lombok.RequiredArgsConstructor;
import lombok.extern.slf4j.Slf4j;
import org.springframework.beans.factory.annotation.Value;
import org.springframework.stereotype.Service;

import java.util.Map;
import java.util.Optional;

@Slf4j
@Service
@RequiredArgsConstructor
public class FileGeneratorService {
    private final Map<String, FileGeneratorHandler> handlerMap;

    @Value("${amazon.folder.name}")
    private String uploadFolder;

    @Value("${amazon.bucket.name}")
    private String bucketName;

    @Value(value = "${amazon.region.name}")
    private String awsRegion;

    @Value(value = "${amazon.file.expiration.time}")
    private String fileExpirationTime;

    @Value(value = "${xml.file.max.row.count}")
    private Integer xmlFileMaxRowCount;

    public GenerateCommandResponseDTO generate(String handlerName, Map<String, Object> parameters) throws RuntimeException {
        FileGeneratorHandler handler = Optional.ofNullable(handlerMap.get(handlerName)).orElseThrow(() -> new IllegalArgumentException("No class handler was found for: {}" + handlerName));

        try {
            return handler.generateFileWithCustomRowCount(bucketName, uploadFolder, awsRegion, Integer.parseInt(fileExpirationTime), parameters, xmlFileMaxRowCount);
        } catch (Exception e) {
            throw new RuntimeException(e);
        }
    }
}


==================================================
File: file-generator-engine/src/main/java/com/papaya/file_generator/engine/FileGeneratorEngineApplication.java
==================================================
package com.papaya.file_generator.engine;

import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;

@SpringBootApplication
public class FileGeneratorEngineApplication {

	public static void main(String[] args) {
		SpringApplication.run(FileGeneratorEngineApplication.class, args);
	}

}


==================================================
File: file-generator-engine/src/main/java/com/papaya/file_generator/handlers/template_based_excel/utils/parser_strategy/ExcelReplacementStrategy.java
==================================================
package com.papaya.file_generator.handlers.template_based_excel.utils.parser_strategy;


import com.papaya.file_generator.handlers.template_based_excel.model.ExcelCellDTO;
import com.papaya.file_generator.handlers.template_based_excel.model.PlaceholderPosition;
import org.apache.poi.xssf.streaming.SXSSFSheet;

public interface ExcelReplacementStrategy {
    void replaceValue(SXSSFSheet sheet, PlaceholderPosition placeholderPosition, ExcelCellDTO excelCellData);

    void applyProperties(SXSSFSheet sheet, PlaceholderPosition placeholderPosition, ExcelCellDTO excelCellData);
}


==================================================
File: file-generator-engine/src/main/java/com/papaya/file_generator/handlers/template_based_excel/utils/parser_strategy/TableExcelReplacementStrategy.java
==================================================
package com.papaya.file_generator.handlers.template_based_excel.utils.parser_strategy;

import com.papaya.file_generator.handlers.template_based_excel.model.ExcelCellDTO;
import com.papaya.file_generator.handlers.template_based_excel.model.ExcelCellTableValueDTO;
import com.papaya.file_generator.handlers.template_based_excel.model.PlaceholderPosition;
import com.papaya.file_generator.handlers.template_based_excel.model.Properties;
import lombok.extern.slf4j.Slf4j;
import org.apache.poi.ss.usermodel.BorderExtent;
import org.apache.poi.ss.usermodel.BorderStyle;
import org.apache.poi.ss.util.CellRangeAddress;
import org.apache.poi.ss.util.PropertyTemplate;
import org.apache.poi.xssf.streaming.SXSSFSheet;

import java.util.List;

@Slf4j
public class TableExcelReplacementStrategy implements ExcelReplacementStrategy {
    public static final String BORDERS = "borders";
    public static final String BORDER_STYLE = "borderStyle";
    public static final String BORDER_EXTENT = "borderExtent";

    @Override
    public void replaceValue(SXSSFSheet sheet, PlaceholderPosition initialPosition, ExcelCellDTO excelTable) {
        ExcelCellTableValueDTO excelCellTableValue = (ExcelCellTableValueDTO) excelTable;

        List<List<ExcelCellDTO>> excelTableData = excelCellTableValue.getValue();


        for (var row = 0; row < excelTableData.size(); row++) {
            for (var col = 0; col < excelTableData.get(row)
                                                  .size(); col++) {
                ExcelCellDTO excelCellData = excelTableData.get(row)
                                                           .get(col);
                ExcelReplacementStrategy replacementStrategy = ValueReplacementStrategyFactory.getStrategy(excelCellData.getClass());
                PlaceholderPosition replacementPosition = new PlaceholderPosition(row + initialPosition.getRowIndex(), col + initialPosition.getColumnIndex());
                replacementStrategy.replaceValue(sheet, replacementPosition, excelCellData);
                replacementStrategy.applyProperties(sheet, replacementPosition, excelCellData);
            }
        }
    }

    @Override
    public void applyProperties(SXSSFSheet sheet, PlaceholderPosition initialPosition, ExcelCellDTO excelCellData) {
        ExcelCellTableValueDTO excelCellTableValue = (ExcelCellTableValueDTO) excelCellData;
        List<List<ExcelCellDTO>> excelTableData = excelCellTableValue.getValue();
        Properties properties = excelCellTableValue.getTableProperties();

        if (properties != null && !properties.isEmpty()
                && Boolean.TRUE.equals(properties.get(BORDERS))) {
            var borderStyle = BorderStyle.MEDIUM;
            var borderExtent = BorderExtent.OUTSIDE;
            if (properties.containsKey(BORDER_STYLE)) {
                borderStyle = BorderStyle.valueOf(String.valueOf(properties.get(BORDER_STYLE)));
            }
            if (properties.containsKey(BORDER_EXTENT)) {
                borderExtent = BorderExtent.valueOf(String.valueOf(properties.get(BORDER_EXTENT)));
            }
            this.applyTableBorder(sheet, initialPosition, excelTableData, borderStyle, borderExtent);

        }

    }

    private void applyTableBorder(SXSSFSheet sheet, PlaceholderPosition initialPosition, List<List<ExcelCellDTO>> excelTableData,
                                  BorderStyle borderStyle, BorderExtent borderExtent) {
        CellRangeAddress cellRangeAddress = new CellRangeAddress(initialPosition.getRowIndex(), initialPosition.getRowIndex() + excelTableData.size() - 1, initialPosition.getColumnIndex(), initialPosition.getColumnIndex() + excelTableData.get(0)
                                                                                                                                                                                                                                              .size() - 1);
        PropertyTemplate propertyTemplate = new PropertyTemplate();
        propertyTemplate.drawBorders(cellRangeAddress, borderStyle, borderExtent);
        propertyTemplate.applyBorders(sheet);

    }
}




==================================================
File: file-generator-engine/src/main/java/com/papaya/file_generator/handlers/template_based_excel/utils/parser_strategy/ValueReplacementStrategyFactory.java
==================================================
package com.papaya.file_generator.handlers.template_based_excel.utils.parser_strategy;


import com.papaya.file_generator.handlers.template_based_excel.model.ExcelCellDTO;
import com.papaya.file_generator.handlers.template_based_excel.model.ExcelCellFormattedValueDTO;
import com.papaya.file_generator.handlers.template_based_excel.model.ExcelCellTableValueDTO;

import java.util.HashMap;
import java.util.Map;


public class ValueReplacementStrategyFactory {
    private static final Map<Class<? extends ExcelCellDTO>, ExcelReplacementStrategy> STRATEGY_FACTORY_MAP = new HashMap<>();

    private ValueReplacementStrategyFactory() {
    }
    static {
        STRATEGY_FACTORY_MAP.put(ExcelCellFormattedValueDTO.class, new ExcelWithFormatReplacementStrategy());
        STRATEGY_FACTORY_MAP.put(ExcelCellTableValueDTO.class, new TableExcelReplacementStrategy());
    }

    public static ExcelReplacementStrategy getStrategy(Class<? extends ExcelCellDTO> classType) {
        return STRATEGY_FACTORY_MAP.get(classType);
    }
}


==================================================
File: file-generator-engine/src/main/java/com/papaya/file_generator/handlers/template_based_excel/utils/parser_strategy/ExcelWithFormatReplacementStrategy.java
==================================================
package com.papaya.file_generator.handlers.template_based_excel.utils.parser_strategy;

import com.papaya.file_generator.handlers.template_based_excel.model.ExcelCellDTO;
import com.papaya.file_generator.handlers.template_based_excel.model.ExcelCellFormattedValueDTO;
import com.papaya.file_generator.handlers.template_based_excel.model.PlaceholderPosition;
import com.papaya.file_generator.handlers.template_based_excel.model.Properties;
import lombok.extern.slf4j.Slf4j;
import org.apache.poi.ss.usermodel.*;
import org.apache.poi.xssf.streaming.SXSSFCell;
import org.apache.poi.xssf.streaming.SXSSFRow;
import org.apache.poi.xssf.streaming.SXSSFSheet;
import org.apache.poi.xssf.streaming.SXSSFWorkbook;

import java.lang.reflect.Field;

@Slf4j
public class ExcelWithFormatReplacementStrategy implements ExcelReplacementStrategy {

    public static final String FONT_COLOR = "fontColor";
    public static final String BOLD = "bold";
    public static final String ITALIC = "italic";
    public static final String COMMENTS = "comments";
    public static final String FONT_SIZE = "fontSize";
    public static final String BACKGROUND_COLOR = "backgroundColor";

    private static short getExcelColorIndex(String colorString) {
        try {
            String indexedColorFieldName = colorString.toUpperCase();
            Field field = IndexedColors.class.getField(indexedColorFieldName);
            IndexedColors indexedColor = (IndexedColors) field.get(null);
            return indexedColor.getIndex();
        } catch (Exception e) {
            return IndexedColors.BLACK.getIndex(); // Default to black if color is not found
        }
    }

    private static SXSSFCell getCell(SXSSFSheet sheet, PlaceholderPosition placeholderPosition) {
        SXSSFRow row = sheet.getRow(placeholderPosition.getRowIndex());
        if (row == null) {
            row = sheet.createRow(placeholderPosition.getRowIndex());
        }
        SXSSFCell cell = row.getCell(placeholderPosition.getColumnIndex());
        if (cell == null) {
            cell = row.createCell(placeholderPosition.getColumnIndex());
        }
        return cell;
    }

    @Override
    public void replaceValue(SXSSFSheet sheet, PlaceholderPosition placeholderPosition, ExcelCellDTO excelCellData) {

        SXSSFCell cell = getCell(sheet, placeholderPosition);

        ExcelCellFormattedValueDTO formattedValueData = (ExcelCellFormattedValueDTO) excelCellData;

        String newValue = formattedValueData.getValue();
        if (newValue != null) {
            cell.setCellValue(newValue);
        }
    }

    @Override
    public void applyProperties(SXSSFSheet sheet, PlaceholderPosition placeholderPosition, ExcelCellDTO excelCellData) {
        SXSSFCell cell = getCell(sheet, placeholderPosition);

        ExcelCellFormattedValueDTO formattedValueData = (ExcelCellFormattedValueDTO) excelCellData;

        Properties properties = formattedValueData.getCellProperties();

        if (properties != null && !properties.isEmpty()) {
            SXSSFWorkbook workbook = sheet.getWorkbook();
            Font font = workbook.createFont();
            CellStyle cellStyle = workbook.createCellStyle();


            if (properties.containsKey(BOLD) && (boolean) properties.get(BOLD)) {
                font.setBold(true);
            }

            if (properties.containsKey(ITALIC)) {
                font.setItalic((boolean) properties.get(ITALIC));
            }

            if (properties.containsKey(COMMENTS)) {
                String comments = properties.get(COMMENTS)
                                            .toString();
                cell.setCellComment(createCellComment(sheet, cell, comments));
            }

            if (properties.containsKey(FONT_COLOR)) {
                String fontColor = properties.get(FONT_COLOR)
                                             .toString();
                font.setColor(getExcelColorIndex(fontColor));
            }

            if (properties.containsKey(FONT_SIZE)) {
                short fontSize = Short.parseShort(properties.get(FONT_SIZE)
                                                            .toString());
                font.setFontHeightInPoints(fontSize);
            }

            if (properties.containsKey(BACKGROUND_COLOR)) {
                String backgroundColor = properties.get(BACKGROUND_COLOR)
                                                   .toString();
                cellStyle
                        .setFillForegroundColor(getExcelColorIndex(backgroundColor));
                cellStyle.setFillBackgroundColor(getExcelColorIndex(backgroundColor));
                cellStyle.setFillPattern(FillPatternType.SOLID_FOREGROUND);
            }


            cellStyle
                    .setFont(font);
            cell.setCellStyle(cellStyle);
        }
    }

    private Comment createCellComment(SXSSFSheet sheet, SXSSFCell cell, String commentText) {
        Drawing drawing = sheet.createDrawingPatriarch();
        CreationHelper factory = sheet.getWorkbook()
                                      .getCreationHelper();

        ClientAnchor anchor = factory.createClientAnchor();
        anchor.setCol1(cell.getColumnIndex());
        anchor.setCol2(cell.getColumnIndex() + 1);
        anchor.setRow1(cell.getRowIndex());
        anchor.setRow2(cell.getRowIndex() + 1);

        Comment comment = drawing.createCellComment(anchor);
        comment.setString(factory.createRichTextString(commentText));
        return comment;
    }

}


==================================================
File: file-generator-engine/src/main/java/com/papaya/file_generator/handlers/template_based_excel/utils/JsonDataParser.java
==================================================
package com.papaya.file_generator.handlers.template_based_excel.utils;

import com.fasterxml.jackson.core.JsonProcessingException;
import com.fasterxml.jackson.databind.ObjectMapper;
import com.papaya.file_generator.handlers.template_based_excel.model.ExcelFileDTO;

import java.io.IOException;
import java.io.InputStream;

public class JsonDataParser {
    private JsonDataParser() {
    }
    public static ExcelFileDTO toObject(InputStream inputStream, Class<ExcelFileDTO> excelFileDTOClass) throws IOException {
        ObjectMapper objectMapper = new ObjectMapper();

        try {
            return objectMapper.readValue(inputStream, excelFileDTOClass);
        } catch (JsonProcessingException jpe) {
            throw new RuntimeException("Failed to parse the json Data", jpe);
        }
    }
}


==================================================
File: file-generator-engine/src/main/java/com/papaya/file_generator/handlers/template_based_excel/utils/ExcelGenerator.java
==================================================
package com.papaya.file_generator.handlers.template_based_excel.utils;

import com.papaya.file_generator.handlers.template_based_excel.model.*;
import com.papaya.file_generator.handlers.template_based_excel.utils.parser_strategy.ExcelReplacementStrategy;
import com.papaya.file_generator.handlers.template_based_excel.utils.parser_strategy.ValueReplacementStrategyFactory;
import org.apache.poi.openxml4j.util.ZipSecureFile;
import org.apache.poi.ss.usermodel.*;
import org.apache.poi.xssf.streaming.SXSSFCell;
import org.apache.poi.xssf.streaming.SXSSFRow;
import org.apache.poi.xssf.streaming.SXSSFSheet;
import org.apache.poi.xssf.streaming.SXSSFWorkbook;
import org.apache.poi.xssf.usermodel.XSSFWorkbook;

import java.io.FileOutputStream;
import java.io.IOException;
import java.io.InputStream;
import java.util.List;
import java.util.Map;
import java.util.Objects;

public final class ExcelGenerator {
    public static final String PLACEHOLDER_PREFIX = "$";
    public static final String HIDDEN = "hidden";
    public static final String WIDTH = "width";
    public static final String AUTO_SIZE = "autoSize";

    private ExcelGenerator() {
    }

    public static void generate(String newFileName, ExcelFileDTO excelFileData, InputStream excelTemplateInputStream, Integer rowSize) throws IOException {
        ZipSecureFile.setMinInflateRatio(-1L);

        XSSFWorkbook excelTemplateWorkbook = new XSSFWorkbook(excelTemplateInputStream);
        try (SXSSFWorkbook newWorkbook = new SXSSFWorkbook(rowSize)) {

            excelFileData.getSheets()
                         .forEach(sheetData -> {
                                     Sheet templateWorkbookSheet = excelTemplateWorkbook.getSheet(sheetData.getSheetName());
                                     if (templateWorkbookSheet != null) {
                                         SXSSFSheet newSheet = newWorkbook.createSheet(templateWorkbookSheet.getSheetName());
                                         newSheet.trackAllColumnsForAutoSizing();
                                         Map<String, ExcelCellDTO> sheetDataMap = sheetData.getSheetData();

                                         ExcelGenerator.copyAndReplace(templateWorkbookSheet, newSheet, sheetDataMap, newWorkbook);
                                         if (sheetData.getSheetProperties() != null) {
                                             ExcelGenerator.applySheetProperties(newSheet, sheetData.getSheetProperties());
                                         }
                                     }
                                 }
                         );

            FileOutputStream fileOutputStream = new FileOutputStream(newFileName);
            newWorkbook.write(fileOutputStream);
            fileOutputStream.close();
            excelTemplateInputStream.close();
            excelTemplateWorkbook.close();
        }
    }

    private static void applySheetProperties(SXSSFSheet newSheet, SheetPropertiesDTO sheetDataMap) {
        List<ColumnPropertiesDTO> columnsProperties = sheetDataMap.getColumnsProperties();

        if (columnsProperties != null) {
            applyColumnsProperties(newSheet, columnsProperties);


        }
    }

    private static void applyColumnsProperties(SXSSFSheet newSheet, List<ColumnPropertiesDTO> columnsProperties) {
        for (ColumnPropertiesDTO columnProperties : columnsProperties) {
            int columnIndex = columnProperties.getColumnIndex();

            Properties properties = columnProperties.getProperties();
            if (properties != null) {
                if (properties.containsKey(HIDDEN)) {
                    newSheet.setColumnHidden(columnIndex - 1, (Boolean) properties.get(HIDDEN));
                }
                if (properties.containsKey(WIDTH)) {
                    newSheet.setColumnWidth(columnIndex - 1, (Integer) properties.get(WIDTH));
                }
                if (properties.containsKey(AUTO_SIZE)) {
                    newSheet.autoSizeColumn(columnIndex - 1, (Boolean) properties.get(AUTO_SIZE));
                }
            }
        }

    }

    private static void copyAndReplace(Sheet templateWorkbookSheet, SXSSFSheet
            newSheet, Map<String, ExcelCellDTO> sheetDataMap, SXSSFWorkbook newWorkbook) {
        SXSSFCell newCell = null;
        int shiftedRows = 0;

        for (Row existingRow : templateWorkbookSheet) {
            SXSSFRow newRow = newSheet.createRow(existingRow.getRowNum() + shiftedRows);

            for (Cell existingCell : existingRow) {
                if (existingCell.getStringCellValue() == null || existingCell.getStringCellValue()
                                                                             .equals("")) {
                    continue;
                }
                if (newRow.getCell(existingCell.getColumnIndex()) == null) {
                    newCell = newRow.createCell(existingCell.getColumnIndex());
                } else
                    newCell = newRow.getCell(existingCell.getColumnIndex());

                copyCellValue(existingCell, newCell, newWorkbook);

                shiftedRows = replaceCellValue(newSheet, sheetDataMap, shiftedRows, existingCell, newCell);
            }
        }

    }

    private static int replaceCellValue(SXSSFSheet newSheet, Map<String, ExcelCellDTO> sheetDataMap,
                                        int shiftedRows, Cell existingCell, SXSSFCell newCell) {
        if (existingCell.getCellType() == CellType.STRING && existingCell.getStringCellValue()
                                                                         .startsWith(PLACEHOLDER_PREFIX)) {
            String placeholderKey = existingCell.getStringCellValue()
                                                .substring(1);

            ExcelCellDTO excelCellData = sheetDataMap.get(placeholderKey);
            if (excelCellData != null) {
                if (excelCellData.getClass() == ExcelCellTableValueDTO.class) {
                    ExcelCellTableValueDTO excelTableData = (ExcelCellTableValueDTO) excelCellData;
                    shiftedRows += excelTableData.getValue()
                                                 .size();
                }

                ExcelReplacementStrategy strategy = ValueReplacementStrategyFactory.getStrategy(excelCellData.getClass());
                if (strategy != null) {
                    PlaceholderPosition placeholderPosition = new PlaceholderPosition(newCell.getRowIndex(), newCell.getColumnIndex());
                    strategy.replaceValue(newSheet, placeholderPosition, excelCellData);
                    strategy.applyProperties(newSheet, placeholderPosition, excelCellData);
                }
            }

        }
        return shiftedRows;
    }

    private static void copyCellValue(Cell existingCell, SXSSFCell newCell, SXSSFWorkbook newWorkbook) {
        CellType cellType = existingCell.getCellType();
        if (Objects.requireNonNull(cellType) == CellType.STRING) {
            newCell.setCellValue(existingCell.getStringCellValue());
        } else if (cellType == CellType.NUMERIC) {
            newCell.setCellValue(existingCell.getNumericCellValue());
        }

        CellStyle existingCellStyle = existingCell.getCellStyle();
        CellStyle newCellStyle = newWorkbook.createCellStyle();
        newCellStyle.cloneStyleFrom(existingCellStyle);
        newCell.setCellStyle(newCellStyle);
    }


}


==================================================
File: file-generator-engine/src/main/java/com/papaya/file_generator/handlers/template_based_excel/model/ExcelSheetDTO.java
==================================================
package com.papaya.file_generator.handlers.template_based_excel.model;

import lombok.Data;

import java.util.Map;
import java.util.TreeMap;

@Data
public class ExcelSheetDTO {
    private String sheetName;

    private SheetPropertiesDTO sheetProperties;

    private Map<String, ExcelCellDTO> sheetData;

    public ExcelSheetDTO() {
        sheetData = new TreeMap<>();
    }

}


==================================================
File: file-generator-engine/src/main/java/com/papaya/file_generator/handlers/template_based_excel/model/ExcelCellValueTypeIdResolver.java
==================================================
package com.papaya.file_generator.handlers.template_based_excel.model;

import com.fasterxml.jackson.annotation.JsonTypeInfo;
import com.fasterxml.jackson.databind.DatabindContext;
import com.fasterxml.jackson.databind.JavaType;
import com.fasterxml.jackson.databind.jsontype.TypeIdResolver;

import java.util.HashMap;
import java.util.Map;
import java.util.Optional;

public class ExcelCellValueTypeIdResolver implements TypeIdResolver {
    private JavaType baseType;
    private Map<String, Class<? extends ExcelCellDTO>> typeMap;

    @Override
    public void init(JavaType baseType) {
        this.baseType = baseType;
        this.typeMap = createTypeMap();
    }

    private Map<String, Class<? extends ExcelCellDTO>> createTypeMap() {
        Map<String, Class<? extends ExcelCellDTO>> map = new HashMap<>();
        map.put("table", ExcelCellTableValueDTO.class);
        map.put("text", ExcelCellFormattedValueDTO.class);

        return map;
    }

    @Override
    public String idFromValue(Object value) {
        return idFromValueAndType(value, value.getClass());
    }

    @Override
    public String idFromValueAndType(Object value, Class<?> suggestedType) {
        Optional<String> matchingKey = typeMap.entrySet()
                .stream()
                .filter(entry -> entry.getValue().isInstance(value))
                .map(Map.Entry::getKey)
                .findFirst();

        return matchingKey.orElseThrow(() -> new IllegalArgumentException("Unsupported type: " + suggestedType.getName()));
    }

    @Override
    public String idFromBaseType() {
        return null;
    }

    @Override
    public JavaType typeFromId(DatabindContext context, String id) {
        Class<? extends ExcelCellDTO> typeClass = typeMap.get(id);
        if (typeClass != null) {
            return context.constructSpecializedType(baseType, typeClass);
        }
        throw new IllegalArgumentException("Unsupported type id: " + id);
    }

    @Override
    public String getDescForKnownTypeIds() {
        return null;
    }

    @Override
    public JsonTypeInfo.Id getMechanism() {
        return JsonTypeInfo.Id.NAME;
    }
}


==================================================
File: file-generator-engine/src/main/java/com/papaya/file_generator/handlers/template_based_excel/model/ExcelCellFormattedValueDTO.java
==================================================
package com.papaya.file_generator.handlers.template_based_excel.model;

import lombok.Getter;
import lombok.NoArgsConstructor;

@Getter
@NoArgsConstructor
public class ExcelCellFormattedValueDTO extends ExcelCellDTO {
    private String value;

    private Properties cellProperties;

    public ExcelCellFormattedValueDTO(String value) {
        this.value = value;
        this.cellProperties = new Properties();
    }

    public ExcelCellDTO setBold() {
        cellProperties.set("bold", true);
        return this;
    }
}


==================================================
File: file-generator-engine/src/main/java/com/papaya/file_generator/handlers/template_based_excel/model/PlaceholderPosition.java
==================================================
package com.papaya.file_generator.handlers.template_based_excel.model;

import lombok.AllArgsConstructor;
import lombok.Data;

@Data
@AllArgsConstructor
public class PlaceholderPosition {
    private int RowIndex;
    private int ColumnIndex;
}


==================================================
File: file-generator-engine/src/main/java/com/papaya/file_generator/handlers/template_based_excel/model/ExcelCellTableValueDTO.java
==================================================
package com.papaya.file_generator.handlers.template_based_excel.model;

import lombok.Getter;
import lombok.Setter;

import java.util.ArrayList;
import java.util.List;

@Setter
@Getter
public class ExcelCellTableValueDTO extends ExcelCellDTO {
    private Properties tableProperties;
    private List<List<ExcelCellDTO>> value;

    public ExcelCellTableValueDTO() {
        this.value = new ArrayList<>();
    }

    public void addRow(List<ExcelCellDTO> tableRow) {
        value.add(tableRow);
    }
}


==================================================
File: file-generator-engine/src/main/java/com/papaya/file_generator/handlers/template_based_excel/model/ColumnPropertiesDTO.java
==================================================
package com.papaya.file_generator.handlers.template_based_excel.model;

import lombok.Data;

@Data
public class ColumnPropertiesDTO {
    private int columnIndex;
    private Properties properties;
}


==================================================
File: file-generator-engine/src/main/java/com/papaya/file_generator/handlers/template_based_excel/model/Properties.java
==================================================
package com.papaya.file_generator.handlers.template_based_excel.model;

import com.fasterxml.jackson.annotation.JsonAnySetter;
import com.fasterxml.jackson.annotation.JsonIgnore;
import lombok.Data;

import java.util.Map;
import java.util.TreeMap;

@Data
public class Properties {
    private final Map<String, Object> properties;

    public Properties() {
        properties = new TreeMap<>();

    }

    @JsonAnySetter
    public void set(String propertyName, Object propertyValue) {
        properties.put(propertyName, propertyValue);
    }

    public boolean containsKey(String propertyName) {
        return properties.containsKey(propertyName);
    }

    public Object get(String propertyName) {
        return properties.get(propertyName);
    }

    @JsonIgnore
    public boolean isEmpty() {
        return properties.isEmpty();
    }
}


==================================================
File: file-generator-engine/src/main/java/com/papaya/file_generator/handlers/template_based_excel/model/ExcelFileDTO.java
==================================================
package com.papaya.file_generator.handlers.template_based_excel.model;

import lombok.Data;

import java.util.ArrayList;
import java.util.List;

@Data
public class ExcelFileDTO {

    private List<ExcelSheetDTO> sheets;

    public ExcelFileDTO() {
        sheets = new ArrayList<>();
    }
    public void addSheet(ExcelSheetDTO sheet) {
        sheets.add(sheet);
    }
}


==================================================
File: file-generator-engine/src/main/java/com/papaya/file_generator/handlers/template_based_excel/model/SheetPropertiesDTO.java
==================================================
package com.papaya.file_generator.handlers.template_based_excel.model;

import lombok.Data;

import java.util.List;

@Data
public class SheetPropertiesDTO {
    private List<ColumnPropertiesDTO> columnsProperties;
}


==================================================
File: file-generator-engine/src/main/java/com/papaya/file_generator/handlers/template_based_excel/model/ExcelCellDTO.java
==================================================
package com.papaya.file_generator.handlers.template_based_excel.model;

import com.fasterxml.jackson.annotation.JsonTypeInfo;
import com.fasterxml.jackson.databind.annotation.JsonTypeIdResolver;
import lombok.Data;

@JsonTypeInfo(use = JsonTypeInfo.Id.NAME, property = "type")
@JsonTypeIdResolver(ExcelCellValueTypeIdResolver.class)
@Data
public class ExcelCellDTO {
}


==================================================
File: file-generator-engine/src/main/java/com/papaya/file_generator/handlers/template_based_excel/TemplateBasedExcelHandler.java
==================================================
package com.papaya.file_generator.handlers.template_based_excel;

import com.papaya.file_generator.commons.exception.ReadFileException;
import com.papaya.file_generator.commons.handler.FileGeneratorHandler;
import com.papaya.file_generator.commons.handler.GenerateCommandResponseDTO;
import com.papaya.file_generator.commons.util.AwsClient;
import com.papaya.file_generator.handlers.template_based_excel.model.ExcelFileDTO;
import com.papaya.file_generator.handlers.template_based_excel.utils.ExcelGenerator;
import com.papaya.file_generator.handlers.template_based_excel.utils.JsonDataParser;
import com.rabbitmq.client.impl.Environment;
import lombok.NoArgsConstructor;
import lombok.extern.slf4j.Slf4j;
import org.springframework.util.ObjectUtils;

import java.io.InputStream;
import java.net.URL;
import java.text.SimpleDateFormat;
import java.util.Date;
import java.util.Map;

@Slf4j
@NoArgsConstructor
public class TemplateBasedExcelHandler implements FileGeneratorHandler {
    public static final String NEW_FILE_NAME = "newFileName";
    public static final String DATA_URL = "dataUrl";
    private static final String TEMPLATE_URL = "templateUrl";
    private static final Integer XLS_MAX_ROW_COUNT = 200;

    private AwsClient awsClient;

    public TemplateBasedExcelHandler(AwsClient awsClient) {
        this.awsClient = awsClient;
    }

    @Override
    public GenerateCommandResponseDTO generateFile(String bucketName, String
            uploadFolder, String awsRegion, int fileExpirationTime    ,Map<String, Object> parameters) throws Exception {
        return generateExcelFile(bucketName, uploadFolder, awsRegion, fileExpirationTime, parameters, 200);
    }
    public GenerateCommandResponseDTO generateExcelFile(String bucketName, String
            uploadFolder, String awsRegion, int fileExpirationTime    ,Map<String, Object> parameters, Integer maxRowSize) throws Exception {
        String templateUrl = (String) parameters.get(TEMPLATE_URL);
        String newFileName = (String) parameters.get(NEW_FILE_NAME);
        String dataUrl = (String) parameters.get(DATA_URL);

        log.info("Start Generating Excel File with maximum row count: {}", maxRowSize);

        if (awsClient == null)
            awsClient = new AwsClient(awsRegion, bucketName);

        try {
            log.info("Accessing bucket {}, folder {}, fileName: {}", bucketName, uploadFolder, templateUrl);
            validateInputData(bucketName, uploadFolder,  templateUrl, awsRegion, newFileName, dataUrl);

            String currentFileName = this.extractFileNameFromPresignedUrl(dataUrl);
            String currentTemplateFileName = this.extractFileNameFromPresignedUrl(templateUrl);
            SimpleDateFormat dateFormat = new SimpleDateFormat("yyyyMMddHHmmss");
            String timestamp = dateFormat.format(new Date());
            log.info("Uploading data");
            awsClient.copyPresignedFile(templateUrl,  uploadFolder + currentFileName + timestamp);
            log.info("Uploading template");
            awsClient.copyPresignedFile(dataUrl, uploadFolder + currentTemplateFileName + timestamp);
            log.info("Reading presigned file: {}", dataUrl);
            InputStream inputJsonData = awsClient.readPresignedFileAsStream(dataUrl);
            ExcelFileDTO excelFileData = JsonDataParser.toObject(inputJsonData, ExcelFileDTO.class);

            InputStream excelTemplateInputStream = awsClient.readPresignedFileAsStream(templateUrl);
            ExcelGenerator.generate(newFileName, excelFileData, excelTemplateInputStream, maxRowSize);
            log.info("Saving generated file: {}", newFileName);
            awsClient.persistData(newFileName,uploadFolder + newFileName );
            log.info("Getting new presinged URL");
            String url = awsClient.getPresignedUrl(uploadFolder + newFileName, fileExpirationTime);
            log.info("File Generated Successfully");
            return new GenerateCommandResponseDTO(url);

        } catch (Throwable e) {
            log.error("Error generating excel file: {}", e.getMessage());
            throw e;
        }
    }

    @Override
    public GenerateCommandResponseDTO generateFileWithCustomRowCount(String bucketName, String
            uploadFolder, String awsRegion, int fileExpirationTime    ,Map<String, Object> parameters, Integer maxRowCount) throws Exception {
        return generateExcelFile(bucketName, uploadFolder, awsRegion, fileExpirationTime, parameters, maxRowCount);
    }

    protected String extractFileNameFromPresignedUrl(String presignedUrl) {
        try {
            URL url = new URL(presignedUrl);

            String path = url.getPath();

            String[] pathSegments = path.split("/");
            return pathSegments[pathSegments.length - 1];
        } catch (Exception e) {
            throw new ReadFileException("Error reading file from pre-signed URL: " + presignedUrl, e);

        }
    }

    private void validateInputData(String bucketName, String uploadFolder, String templateUrl, String awsRegion, String
            newFileName, String dataUrl) {
        if (bucketName == null || bucketName.isEmpty()) {
            throw new IllegalArgumentException("Bucket name is required");
        }
        if (uploadFolder == null || uploadFolder.isEmpty()) {
            throw new IllegalArgumentException("Upload folder is required");
        }
        if (templateUrl == null || templateUrl.isEmpty()) {
            throw new IllegalArgumentException("Template url is required");
        }
        if (newFileName == null || newFileName.isEmpty()) {
            throw new IllegalArgumentException("New file name is required");
        }
        if (dataUrl == null || dataUrl.isEmpty()) {
            throw new IllegalArgumentException("Data url is required");
        }
        if (awsRegion == null || awsRegion.isEmpty()) {
            throw new IllegalArgumentException("AWS Region is required");
        }
    }
}

