# Android Architecture

## 概述

该项目结合 MVP 与 Clean 架构思想，探索在 Android 项目上的最佳实践。

遵循 [Clean Architecture](https://blog.8thlight.com/uncle-bob/2012/08/13/the-clean-architecture.html) 的原则。

<img src="https://github.com/jeanboydev/Android-Architecture/blob/master/resources/images/android-architecture.png" alt="architecture"/>

- 数据层（Data Layer）：加入数据转换层（Mapper）将服务端数据模型（Entity）与本地数据模型（Model）解耦。
- 业务层（Domain Layer）：按模块划分业务，具体业务交给 Usecase 处理。
- 显示层（View Layer）： Presenter 不再与 Activity/Fragment 一一对应，Presenter 按照业务模块划分功能，大大提高 Presenter 的复用性。Activity/Fragment 中可以实现多个 View，持有多个 Presenter 来完成业务逻辑。

## 示例

| 分支 | 描述 |
| ------------- | ------------- |
| [master](https://github.com/jeanboydev/Android-Architecture) | 演示了 Model-View-Presenter（MVP）+ Clean 架构，提供一些基类，状态栏沉浸适配等 |
| [develop](https://github.com/jeanboydev/Android-Architecture/tree/develop) | 使用 [butterknife](https://github.com/JakeWharton/butterknife) |
| [develop-dagger](https://github.com/jeanboydev/Android-Architecture/tree/develop-dagger) | 加入 [dagger](https://github.com/google/dagger) 的支持 |
| [develop-dagger-rxjava](https://github.com/jeanboydev/Android-Architecture/tree/develop-dagger-rxjava) | 加入 [rxjava](https://github.com/ReactiveX/RxJava) 的支持 |

## 项目结构

项目结构思维导图
<img src="https://github.com/jeanboydev/Android-Architecture/blob/master/resources/images/android_project.png" alt="architecture"/>

## 参考资料
[Android 开发规范](https://github.com/Blankj/AndroidStandardDevelop)

[android-architecture](https://github.com/googlesamples/android-architecture)

[Android-CleanArchitecture](https://github.com/android10/Android-CleanArchitecture)

## License

    Copyright 2016 jeanboy

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.