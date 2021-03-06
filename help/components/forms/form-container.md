---
title: Form Container Component
description: The Core Component Form Container Component allows for the creation of simple submission forms.
---

# Form Container Component {#form-container-component}

The Core Component Form Container Component allows for the creation of simple submission forms.

## Usage {#usage}

The form Container Component enables the building of simple information submission forms and features by supporting simple WCM forms and by using a nested structure to allow additional form components.

By using the [configure dialog](#configure-dialog) the content editor can define the action triggered by form submission, where the submitted content should be stored, and whether a workflow should be triggered. The template author can use the [design dialog](#design-dialog) to define the allowed components and their mappings similar to the design dialog for the [standard layout container in the template editor](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html).

>[!NOTE]
>
>The core components Form Container Component only supports the use of core components form components (button, text, hidden, etc.). Using [foundation components](https://docs.adobe.com/content/help/en/experience-manager-65/authoring/siteandpage/default-components-foundation.html) form components within the core components form container (and vice versa) is not supported.

## Version and Compatibility {#version-and-compatibility}

The current version of the Form Container Component is v2, which was introduced with release 2.0.0 of the Core Components in January 2018, and is described in this document.

The following table details all supported versions of the component, the AEM versions with which the versions of the component is compatible, and links to documentation for previous versions.

|Component Version|AEM 6.3|AEM 6.4|AEM 6.5|AEM as a Cloud Service|
|--- |--- |--- |--- |---|
|v2|Compatible|Compatible|Compatible|Compatible|
|[v1](/help/components/v1/form-container-v1.md)|Compatible|Compatible|Compatible|-|

For more information about Core Component versions and releases, see the document [Core Components Versions](/help/versions.md).

## Technical Details {#technical-details}

The latest technical documentation about the Form Container Component [can be found on GitHub](https://adobe.com/go/aem_cmp_tech_form_container_v2).

Further details about developing Core Components can be found in the [Core Components developer documentation](/help/developing/overview.md).

## Configure Dialog {#configure-dialog}

The configure dialog allows the content author to define what actions are taken when the component is submitted.

![](/help/assets/screen_shot_2018-01-12at122046.png)

Depending on the selected **Action Type**, the available options within the container will change. The available action types are:

* [Mail](#mail)
* [Store Content](#store-content)
* [Submit Order](#submit-order)
* [Update Order](#update-order)

Regardless of the type, there are [general settings](#general-settings) that apply to each action.

### Mail {#mail}

When the form is submitted, the mail action type will send an email to designated recipients.

![](/help/assets/screen_shot_2018-01-12at122554.png)

* **Subject**
  The subject of the email that will be sent on form submission
* **From**
  The from email address of the email that will be send on form submission
* **To**
  The addresses of the recipients who will receive an email upon form submission

  * Tap or click the **Add** button to add additional addresses
  * Tap or click the **Delete** button to remove an email address
* **CC**
  The addresses of recipients who will receive a carbon copy the email sent upon form submission
  * Tap or click the **Add** button to add additional addresses
  * Tap or click the **Delete** button to remove an email address

### Store Content {#store-content}

When the form is submitted, the content of the form will be stored in a designated repository location.

![](/help/assets/screen_shot_2018-01-12at122538.png)

* **Content Path**
  Content repository path where submitted content is stored
* **View Data**
  Tap or click to view stored submitted data as JSON
* **Start Workflow**
  Configure to start a workflow with the stored content as payload upon form submission

### Submit Order {#submit-order}

When the form is submitted, the order will be submitted.

![](/help/assets/chlimage_1-3.png)

### Update Order {#update-order}

When the form is submitted, the order will be updated.

![](/help/assets/chlimage_1-4.png)

### General Settings {#general-settings}

Regardless of the action type selected, a thank you page can always be defined.

![](/help/assets/chlimage_1-5.png)

The user will be redirected to the specified page after completion of the form submission.

* Use the Selection Dialog to select a resource within AEM.
* If the thank you page is not in AEM, specify the absolute URL. Non-absolute URLs will be interpreted relative to AEM.
* Leave blank to redisplay the form after submission.

## Design Dialog {#design-dialog}

The design dialog allows the template author to define the allowed components and their mappings for the container similar to the design dialog for the [standard layout container in the template editor](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html).
