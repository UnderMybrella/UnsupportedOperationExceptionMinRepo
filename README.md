# UnsupportedOperationExceptionMinRepo
A minimum reproduction of an UnsupportedOperationException thrown by IntelliJ when importing Multiplatform Projects

Attempting to (re)load this project in Intellij 2020.1 throws the following exception:

```
Cause: java.lang.UnsupportedOperationException
	at java.base/java.util.Collections$1.remove(Collections.java:4714)
	at java.base/java.util.AbstractSet.removeAll(AbstractSet.java:176)
	at org.jetbrains.plugins.gradle.service.project.GradleProjectResolverUtil.doBuildDependencies(GradleProjectResolverUtil.java:646)
	at org.jetbrains.plugins.gradle.service.project.GradleProjectResolverUtil.buildDependencies(GradleProjectResolverUtil.java:565)
	at org.jetbrains.kotlin.idea.configuration.KotlinMPPGradleProjectResolver$Companion$populateModuleDependencies$1.invoke(KotlinMPPGradleProjectResolver.kt:543)
	at org.jetbrains.kotlin.idea.configuration.KotlinMPPGradleProjectResolver$Companion$populateModuleDependencies$1.invoke(KotlinMPPGradleProjectResolver.kt:185)
	at org.jetbrains.kotlin.idea.configuration.KotlinMPPGradleProjectResolver$Companion.processCompilations(KotlinMPPGradleProjectResolver.kt:799)
	at org.jetbrains.kotlin.idea.configuration.KotlinMPPGradleProjectResolver$Companion.populateModuleDependencies(KotlinMPPGradleProjectResolver.kt:539)
	at org.jetbrains.kotlin.idea.configuration.KotlinMPPGradleProjectResolver.populateModuleDependencies(KotlinMPPGradleProjectResolver.kt:153)
	at org.jetbrains.plugins.gradle.service.project.AbstractProjectResolverExtension.populateModuleDependencies(AbstractProjectResolverExtension.java:105)
	at org.jetbrains.plugins.gradle.service.project.AbstractProjectResolverExtension.populateModuleDependencies(AbstractProjectResolverExtension.java:105)
	at org.jetbrains.plugins.gradle.service.project.AbstractProjectResolverExtension.populateModuleDependencies(AbstractProjectResolverExtension.java:105)
	at org.jetbrains.plugins.gradle.service.project.AbstractProjectResolverExtension.populateModuleDependencies(AbstractProjectResolverExtension.java:105)
	at org.jetbrains.plugins.gradle.service.project.AbstractProjectResolverExtension.populateModuleDependencies(AbstractProjectResolverExtension.java:105)
	at org.jetbrains.plugins.gradle.service.project.AbstractProjectResolverExtension.populateModuleDependencies(AbstractProjectResolverExtension.java:105)
	at com.android.tools.idea.gradle.project.sync.idea.AndroidGradleProjectResolver.populateModuleDependencies(AndroidGradleProjectResolver.java:458)
	at org.jetbrains.plugins.gradle.service.project.AbstractProjectResolverExtension.populateModuleDependencies(AbstractProjectResolverExtension.java:105)
	at org.jetbrains.plugins.gradle.service.project.AbstractProjectResolverExtension.populateModuleDependencies(AbstractProjectResolverExtension.java:105)
	at org.jetbrains.plugins.gradle.service.project.AbstractProjectResolverExtension.populateModuleDependencies(AbstractProjectResolverExtension.java:105)
	at org.jetbrains.plugins.gradle.service.project.AbstractProjectResolverExtension.populateModuleDependencies(AbstractProjectResolverExtension.java:105)
	at org.jetbrains.plugins.gradle.service.project.AbstractProjectResolverExtension.populateModuleDependencies(AbstractProjectResolverExtension.java:105)
	at org.jetbrains.plugins.gradle.service.project.AbstractProjectResolverExtension.populateModuleDependencies(AbstractProjectResolverExtension.java:105)
	at org.jetbrains.plugins.gradle.service.project.AbstractProjectResolverExtension.populateModuleDependencies(AbstractProjectResolverExtension.java:105)
	at org.jetbrains.kotlin.idea.configuration.KotlinGradleProjectResolverExtension.populateModuleDependencies(KotlinGradleProjectResolverExtension.kt:217)
	at org.jetbrains.plugins.gradle.service.project.AbstractProjectResolverExtension.populateModuleDependencies(AbstractProjectResolverExtension.java:105)
	at org.jetbrains.plugins.gradle.service.project.AbstractProjectResolverExtension.populateModuleDependencies(AbstractProjectResolverExtension.java:105)
	at org.jetbrains.kotlin.android.configure.KotlinAndroidMPPGradleProjectResolver.populateModuleDependencies(KotlinAndroidMPPGradleProjectResolver.kt:54)
	at org.jetbrains.plugins.gradle.service.project.AbstractProjectResolverExtension.populateModuleDependencies(AbstractProjectResolverExtension.java:105)
	at org.jetbrains.plugins.gradle.service.project.AbstractProjectResolverExtension.populateModuleDependencies(AbstractProjectResolverExtension.java:105)
	at org.jetbrains.plugins.gradle.service.project.AbstractProjectResolverExtension.populateModuleDependencies(AbstractProjectResolverExtension.java:105)
	at org.jetbrains.plugins.gradle.service.project.TracedProjectResolverExtension.populateModuleDependencies(TracedProjectResolverExtension.java:72)
	at org.jetbrains.plugins.gradle.service.project.GradleProjectResolver.doResolveProjectInfo(GradleProjectResolver.java:396)
	at org.jetbrains.plugins.gradle.service.project.GradleProjectResolver.access$200(GradleProjectResolver.java:61)
	at org.jetbrains.plugins.gradle.service.project.GradleProjectResolver$ProjectConnectionDataNodeFunction.fun(GradleProjectResolver.java:720)
	at org.jetbrains.plugins.gradle.service.project.GradleProjectResolver$ProjectConnectionDataNodeFunction.fun(GradleProjectResolver.java:703)
	at org.jetbrains.plugins.gradle.service.execution.GradleExecutionHelper.execute(GradleExecutionHelper.java:269)
	at org.jetbrains.plugins.gradle.service.project.GradleProjectResolver.resolveProjectInfo(GradleProjectResolver.java:139)
	at org.jetbrains.plugins.gradle.service.project.GradleProjectResolver.resolveProjectInfo(GradleProjectResolver.java:61)
	at com.intellij.openapi.externalSystem.service.remote.RemoteExternalSystemProjectResolverImpl.lambda$resolveProjectInfo$0(RemoteExternalSystemProjectResolverImpl.java:37)
	at com.intellij.openapi.externalSystem.service.remote.AbstractRemoteExternalSystemService.execute(AbstractRemoteExternalSystemService.java:57)
	at com.intellij.openapi.externalSystem.service.remote.RemoteExternalSystemProjectResolverImpl.resolveProjectInfo(RemoteExternalSystemProjectResolverImpl.java:36)
	at com.intellij.openapi.externalSystem.service.remote.wrapper.ExternalSystemProjectResolverWrapper.resolveProjectInfo(ExternalSystemProjectResolverWrapper.java:46)
	at com.intellij.openapi.externalSystem.service.internal.ExternalSystemResolveProjectTask.doExecute(ExternalSystemResolveProjectTask.java:102)
	at com.intellij.openapi.externalSystem.service.internal.AbstractExternalSystemTask.execute(AbstractExternalSystemTask.java:147)
	at com.intellij.openapi.externalSystem.service.internal.AbstractExternalSystemTask.execute(AbstractExternalSystemTask.java:133)
	at com.intellij.openapi.externalSystem.util.ExternalSystemUtil$2.executeImpl(ExternalSystemUtil.java:520)
	at com.intellij.openapi.externalSystem.util.ExternalSystemUtil$2.lambda$execute$1(ExternalSystemUtil.java:372)
	at com.intellij.openapi.project.DumbServiceImpl.suspendIndexingAndRun(DumbServiceImpl.java:171)
	at com.intellij.openapi.externalSystem.util.ExternalSystemUtil$2.execute(ExternalSystemUtil.java:372)
	at com.intellij.openapi.externalSystem.util.ExternalSystemUtil$4.run(ExternalSystemUtil.java:627)
	at com.intellij.openapi.progress.impl.CoreProgressManager$TaskRunnable.run(CoreProgressManager.java:932)
	at com.intellij.openapi.progress.impl.CoreProgressManager.lambda$runProcessWithProgressAsync$5(CoreProgressManager.java:434)
	at com.intellij.openapi.progress.impl.ProgressRunner.lambda$null$3(ProgressRunner.java:233)
	at com.intellij.openapi.progress.impl.CoreProgressManager.lambda$runProcess$2(CoreProgressManager.java:166)
	at com.intellij.openapi.progress.impl.CoreProgressManager.registerIndicatorAndRun(CoreProgressManager.java:627)
	at com.intellij.openapi.progress.impl.CoreProgressManager.executeProcessUnderProgress(CoreProgressManager.java:572)
	at com.intellij.openapi.progress.impl.ProgressManagerImpl.executeProcessUnderProgress(ProgressManagerImpl.java:61)
	at com.intellij.openapi.progress.impl.CoreProgressManager.runProcess(CoreProgressManager.java:153)
	at com.intellij.openapi.progress.impl.ProgressRunner.lambda$submit$4(ProgressRunner.java:233)
	at java.base/java.util.concurrent.CompletableFuture$AsyncSupply.run(CompletableFuture.java:1700)
	at java.base/java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1128)
	at java.base/java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:628)
	at java.base/java.lang.Thread.run(Thread.java:834)
  ```
