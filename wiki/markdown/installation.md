# Installation

Eiffel REMReM Publish is maven project and can be built by executing following command:

```
mvn clean install
```

Binary is released via [jitPack](https://jitpack.io/#eiffel-community/eiffel-remrem-publish).

The latest REMReM Publish CLI binary can be downloaded via [publish-cli.jar](https://jitpack.io/#eiffel-community/eiffel-remrem-publish).

The latest REMReM Publish Service binary can be downloaded via [publish-service.war](https://jitpack.io/#eiffel-community/eiffel-remrem-publish).

The latest REMReM Publish uses the routing key structure defined in [Eiffel Sepia](https://eiffel-community.github.io/eiffel-sepia/rabbitmq-message-broker.html).
To make it compatible to prior routing key structure
create a file at desired location : path/to/routing-key-overrides.properties
with the below mappings and pass the file location to the jar as follows

Ex: java -DsemanticsRoutingKeyTypeOverrideFilepath=path/to/routing-key-overrides.properties -jar publish-service.war

#########Mappings in routing-key-overrides.properties#############

EiffelActivityCanceledEvent.family=activity
EiffelActivityCanceledEvent.type=canceled

EiffelActivityFinishedEvent.family=activity
EiffelActivityFinishedEvent.type=finished

EiffelActivityStartedEvent.family=activity
EiffelActivityStartedEvent.type=started

EiffelActivityTriggeredEvent.family=activity
EiffelActivityTriggeredEvent.type=triggered

EiffelAnnouncementPublishedEvent.family=info
EiffelAnnouncementPublishedEvent.type=announcement

EiffelArtifactCreatedEvent.family=artifact
EiffelArtifactCreatedEvent.type=created

EiffelArtifactPublishedEvent.family=artifact
EiffelArtifactPublishedEvent.type=published

EiffelArtifactReusedEvent.family=artifact
EiffelArtifactReusedEvent.type=reused

EiffelCompositionDefinedEvent.family=cm
EiffelCompositionDefinedEvent.type=composition

EiffelConfidenceLevelModifiedEvent.family=artifact
EiffelConfidenceLevelModifiedEvent.type=modified

EiffelEnvironmentDefinedEvent.family=cm
EiffelEnvironmentDefinedEvent.type=environment

EiffelFlowContextDefinedEvent.family=flowcontext
EiffelFlowContextDefinedEvent.type=defined

EiffelIssueVerifiedEvent.family=test
EiffelIssueVerifiedEvent.type=issueverified

EiffelSourceChangeCreatedEvent.family=cm
EiffelSourceChangeCreatedEvent.type=scmchange

EiffelSourceChangeSubmittedEvent.family=cm
EiffelSourceChangeSubmittedEvent.type=scmproposedchange

EiffelTestCaseCanceledEvent.family=test
EiffelTestCaseCanceledEvent.type=casecanceled

EiffelTestCaseTriggeredEvent.family=test
EiffelTestCaseTriggeredEvent.type=casetriggered

EiffelTestCaseFinishedEvent.family=test
EiffelTestCaseFinishedEvent.type=casefinished

EiffelTestCaseStartedEvent.family=test
EiffelTestCaseStartedEvent.type=casestarted

EiffelTestSuiteFinishedEvent.family=test
EiffelTestSuiteFinishedEvent.type=suitefinished

EiffelTestSuiteStartedEvent.family=test
EiffelTestSuiteStartedEvent.type=suitestarted

EiffelTestExecutionRecipeCollectionCreatedEvent.family=test
EiffelTestExecutionRecipeCollectionCreatedEvent.type=execution

EiffelAlertAcknowledgedEvent.family=alert
EiffelAlertAcknowledgedEvent.type=alertack

EiffelArtifactDeployedEvent.family=artifact
EiffelArtifactDeployedEvent.type=deployed

EiffelServiceAllocatedEvent.family=service
EiffelServiceAllocatedEvent.type=allocated

EiffelServiceDeployedEvent.family=service
EiffelServiceDeployedEvent.type=deployed

EiffelServiceDiscontinuedEvent.family=service
EiffelServiceDiscontinuedEvent.type=discontinued

EiffelServiceReturnedEvent.family=service
EiffelServiceReturnedEvent.type=returned

EiffelServiceStartedEvent.family=service
EiffelServiceStartedEvent.type=started

EiffelServiceStoppedEvent.family=service
EiffelServiceStoppedEvent.type=stopped

EiffelAlertRaisedEvent.family=alert
EiffelAlertRaisedEvent.type=raised

EiffelAlertCeasedEvent.family=alert
EiffelAlertCeasedEvent.type=ceased

EiffelIssueDefinedEvent.family=test
EiffelIssueDefinedEvent.type=issuedefined


