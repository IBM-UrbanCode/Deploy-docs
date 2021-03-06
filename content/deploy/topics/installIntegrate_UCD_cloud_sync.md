# Integrating IBM UrbanCode™ Deploy with UrbanCode Mobile {#installIntegrate_UCD_cloud_sync .task}

Use IBM® Bluemix™ DevOps Connect to integrate IBM UrbanCode® Deploy with UrbanCode Mobile.

Make sure the IBM UrbanCode Deploy for Mobile plug-in is installed in IBM Bluemix DevOps Connect.

After you run an integration, first-time eligible users receive email invitations to download and register the UrbanCode Mobile application. Users are eligible if they are members of teams that run deployments. For best results, configure the IBM UrbanCode Deploy teams before you run an integration. The email that users receive contains a link where users can download the app, and an access code they can use to register their mobile application. After they register their mobile application, users receive deployment data from the cloud-based service. For information about registering the mobile app, see [Configuring the UrbanCode Mobile app](installIntegrate_UCR_mobile.md#).

In the IBM UrbanCode Deploy instance, generate a token for the admin user. You use the token to authenticate the IBM UrbanCode Deploy instance.

Use the IBM UrbanCode Deploy for Mobile plug-in to create integrations that provide IBM UrbanCode Deploy deployment data to the UrbanCode Mobile app. Integrations send summary deployment data to the IBM Cloud Service through an encrypted SSL connection, and store the data in an encrypted database. The encrypted data is provided to UrbanCode Mobile users.

1.   From the IBM Bluemix DevOps Connect dashboard, click **Integrations**, and then click **Add New**. 
2.  In the **Name** field, type a name for the integration.
3.   From the **Integration Type** list, select **IBM UrbanCode Deploy for mobile**. Fields that are related to your selection are displayed. The **Version** field displays the plug-in version number.
4.   In the **Server URI** field, enter the public URL of the IBM UrbanCode Deploy server. For example, `https://my\_UCD.com:8447`.
5.   In the **Authentication Token** field, enter or paste the authentication token generated by IBM UrbanCode Deploy. 
6.   In the **Frequency** field, specify the integration frequency. Integrations run on an interval determined by the entered value. The default value is 1 minute, which means that integrations run every minute.
7.   Click **Run Integration** to run the integration immediately. You can manually run integrations at any time regardless of the value in the **Frequency** field.
8.   Click **Save**. 

After the integration runs, deployment data for the selected phases is synced with the IBM Cloud Service. Eligible first-time users receive email invitations to download the mobile app.

If you are a first-time user of the mobile app, see [Configuring the UrbanCode Mobile app](installIntegrate_UCR_mobile.md#).

**Parent topic:** [Integrating with cloud and mobile services with IBM BluemixIBM DevOps Connect](../topics/installIntegrate_UCR_cloud_cp.md)

