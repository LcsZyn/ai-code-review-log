### 代码评审报告

#### 文件：`.github/workflows/main-maven-jar.yml`

**变更点：**
- 添加了获取仓库名称、分支名称、提交作者和提交信息的步骤。
- 在`Run Code Review`步骤中添加了环境变量，用于传递获取到的信息。

**评审意见：**
- 添加获取信息的步骤是一个好的实践，它可以帮助记录和跟踪代码更改。
- 在`Run Code Review`步骤中添加环境变量是一个很好的方式，可以让代码更加灵活。
- 建议在`Run Code Review`步骤中添加对环境变量的校验，确保它们不为空。

#### 文件：`ai-code-review-sdk/src/main/java/cn/bugstack/ai/sdk/OpenAiCodeReview.java`

**变更点：**
- 将主函数中的代码拆分到不同的方法和类中。
- 添加了新的类和接口，如`GitCommand`、`IOpenAI`、`WeiXin`、`AbstractOpenAiCodeReviewService`、`IOpenAiCodeReviewService`、`OpenAiCodeReviewService`。

**评审意见：**
- 将代码拆分到不同的方法和类中是一个好的实践，它可以提高代码的可读性和可维护性。
- 添加新的类和接口是一个好的设计，它可以提高代码的模块化和可复用性。
- 建议在`GitCommand`、`IOpenAI`、`WeiXin`类中添加异常处理，确保代码的健壮性。
- 建议在`AbstractOpenAiCodeReviewService`类中添加抽象方法，让子类实现具体的逻辑。

#### 文件：`ai-code-review-sdk/src/main/java/cn/bugstack/ai/sdk/domain/service/AbstractOpenAiCodeReviewService.java`

**变更点：**
- 添加了一个抽象类`AbstractOpenAiCodeReviewService`，它定义了代码评审服务的公共接口。

**评审意见：**
- 添加抽象类是一个好的设计，它可以提高代码的模块化和可复用性。
- 建议在抽象类中添加更多的抽象方法，例如获取代码、记录评审结果、发送消息通知等。

#### 文件：`ai-code-review-sdk/src/main/java/cn/bugstack/ai/sdk/domain/service/IOpenAiCodeReviewService.java`

**变更点：**
- 添加了一个接口`IOpenAiCodeReviewService`，它定义了代码评审服务的公共接口。

**评审意见：**
- 添加接口是一个好的设计，它可以提高代码的模块化和可复用性。
- 建议在接口中添加更多的方法，例如获取代码、记录评审结果、发送消息通知等。

#### 文件：`ai-code-review-sdk/src/main/java/cn/bugstack/ai/sdk/domain/service/impl/OpenAiCodeReviewService.java`

**变更点：**
- 实现了`IOpenAiCodeReviewService`接口，并实现了具体的代码评审逻辑。

**评审意见：**
- 实现接口是一个好的设计，它可以提高代码的模块化和可复用性。
- 建议在实现类中添加异常处理，确保代码的健壮性。

#### 文件：`ai-code-review-sdk/src/main/java/cn/bugstack/ai/sdk/infrastructure/git/GitCommand.java`

**变更点：**
- 添加了一个`GitCommand`类，它提供了与Git相关的操作。

**评审意见：**
- 添加`GitCommand`类是一个好的设计，它可以提高代码的模块化和可复用性。
- 建议在`GitCommand`类中添加更多的方法，例如获取提交历史、获取代码变更等。

#### 文件：`ai-code-review-sdk/src/main/java/cn/bugstack/ai/sdk/infrastructure/openai/IOpenAI.java`

**变更点：**
- 添加了一个接口`IOpenAI`，它定义了与OpenAI API交互的公共接口。

**评审意见：**
- 添加接口是一个好的设计，它可以提高代码的模块化和可复用性。
- 建议在接口中添加更多的方法，例如发送代码评审请求、获取代码评审结果等。

#### 文件：`ai-code-review-sdk/src/main/java/cn/bugstack/ai/sdk/infrastructure/openai/dto/ChatCompletionRequestDTO.java`

**变更点：**
- 添加了一个DTO类`ChatCompletionRequestDTO`，它表示发送给OpenAI API的请求。

**评审意见：**
- 添加DTO类是一个好的设计，它可以提高代码的可读性和可维护性。
- 建议在DTO类中添加更多的字段，例如请求的模型、消息等。

#### 文件：`ai-code-review-sdk/src/main/java/cn/bugstack/ai/sdk/infrastructure/openai/dto/ChatCompletionSyncResponseDTO.java`

**变更