---

copyright:
  years: 2016, 2018
lastupdated: "2018-07-19"

---

{:new_window: target="\_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:codeblock: .codeblock}
{:pre: .pre}

# Connecting and configuring a historian connector to use {{site.data.keyword.messagehub}}  
{: #messagehub_main}

Connecting {{site.data.keyword.messagehub_full}} to {{site.data.keyword.iot_full}} provides a scalable, high-throughput message bus for historical data storage. {{site.data.keyword.messagehub}} is built on Apache Kafka, which is an open-source, high-throughput messaging system that provides a low-latency platform for handling real-time data feeds.

{{site.data.keyword.messagehub}} forwarding partitions events by using a partition key. The key is formed by concatenating the {{site.data.keyword.iot_short}} 6 character organization ID with the device type and device ID. Payload fields, including timestamp and event ID, are not used to form the partition key. This configuration ensures that all events from a specific device are sent to the same partition, so that the events are processed in the order in which they are sent. 

The quality of service (QoS) that is used by an MQTT device to send messages to {{site.data.keyword.iot_short_notm}} does not apply when messages are sent from {{site.data.keyword.iot_short_notm}} to {{site.data.keyword.messagehub}}. Typically, a message is sent to {{site.data.keyword.messagehub}} once. Rarely, it might be possible for a message to be sent more than once or not at all.

## Before you begin  
{: #byb}

Before connecting an {{site.data.keyword.messagehub}} instance to {{site.data.keyword.iot_short}}, complete the following tasks:

- Set up {{site.data.keyword.messagehub}} in the same {{site.data.keyword.Bluemix_notm}} space as your {{site.data.keyword.iot_short_notm}} by using the {{site.data.keyword.Bluemix_notm}} Catalog. For more information about {{site.data.keyword.messagehub}}, see the [Getting started with {{site.data.keyword.messagehub}}](https://console.{DomainName}/docs/services/MessageHub/index.html).

- Ensure that you have developer privileges in the {{site.data.keyword.Bluemix_notm}} organization and that you are signed in via {{site.data.keyword.Bluemix_notm}}. If you are not signed in through {{site.data.keyword.Bluemix_notm}}, or do not have developer privileges in this {{site.data.keyword.Bluemix_notm}} organization, you are not able to authorize the binding of {{site.data.keyword.messagehub}} and the {{site.data.keyword.iot_short_notm}}.


## Connect

To connect {{site.data.keyword.messagehub}} for historical data storage:

1. On your {{site.data.keyword.iot_short}} dashboard click **Extensions** in the navigation bar.
2. In the Historical Data Storage tile, click **Setup**.
4. Select the {{site.data.keyword.messagehub}} service that you want to connect.  
All available {{site.data.keyword.messagehub}} services within the same {{site.data.keyword.Bluemix_notm}} space as your {{site.data.keyword.iot_short}} service are listed in the Configure historical data storage section.
5. Select your {{site.data.keyword.messagehub}} configuration options:
 1. Select a time zone.  
 The timestamps on the device data that is sent to the {{site.data.keyword.messagehub}} are converted to the selected timezone.
 2. Select a default topic.  
 Device events are sent to the default topic if one is defined here. To use more granular topic assignments, leave the default topic blank and add custom forwarding rules.
 3. Optional: Specify custom forwarding rules.  
 Specify additional rules for forwarding device events. Only events that match the custom forwarding rules are forwarded.  
 **Note:** An event might match multiple forwarding rules and be forwarded to multiple {{site.data.keyword.messagehub}} topics.
 4. Optional: Configure topics.  
 To create the topics with more than the default two partitions, you can specify the partition configuration.
 5. Click **Done**.
5. Click **Authorize**.
6. In the Authorization dialog box, click **Confirm**.

Your device data is now stored in your {{site.data.keyword.messagehub}} instance.
