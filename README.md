Welcome to use this program to monitor your sense jobs.

You need to put these two files together in any directory on the server. Before running, there are several steps to configure.

- Step 1:

    - You need to create your own virtual proxy account in the qmc system as marked in the pictures below. 
    ![pic1](https://github.com/mxxt/my_image/blob/master/sense_task0.png?raw=true)

    - It should be noted that you need to fill in **task** in **Prefix** input box, as marked in the second picture.
    ![pic2](https://github.com/mxxt/my_image/blob/master/sense_task1.png?raw=true)

    - You can add cluster node addresses to monitor the jobs of all child nodes.
    ![pic3](https://github.com/mxxt/my_image/blob/master/sense_task2.png?raw=true)

- Step 2:

    - Open the **JobAlertConf.exe** file to set monitoring options.
    ![pic4](https://github.com/mxxt/my_image/blob/master/sense_conf_1.jpeg?raw=true)

    - Click the **Add** drop-down box and select whether to add monitoring or key jobs.
    ![pic5](https://github.com/mxxt/my_image/blob/master/sense_conf_2.jpeg?raw=true)

    - Take adding monitoring job as an example.Fill in the **Cluster IP** and the **Cluster User**, which is the input box named **Hearder authentication header name** filled in qmc), then click the **getJobList** button to get all the jobs in the cluster. You can select some jobs to add to the monitoring job list on the right, or you can add them all at once. If you need to add a job failure log file to the email attachment, you need to check the option **AttachLogFile**.
    ![pic7](https://github.com/mxxt/my_image/blob/master/sense_conf_9.jpeg?raw=true)
    If you want to monitor a certain type of jobs, you can fill in the prefix word in the **Prefix** input box.

    - Click the **Save** button to save the data.
    After returning to the main interface, you can see the data just filled in.
    ![pic9](https://github.com/mxxt/my_image/blob/master/sense_conf_10.jpeg?raw=true)

- Step 3:
    - Now You can start filling out the mail configuration.
    You need to fill in the **SMTP** address and **Port**. If you need the SSL encryption protocol, you need to check the **SSL** checkbox. You need to fill in the sender's email address and password, and the recipient's email address and you can use ; to separate multiple email addresses.
    ![pic10](https://github.com/mxxt/my_image/blob/master/sense_conf_11.jpeg?raw=true)
    After filling in, click the **Save** button.

    - If you have purchased this product, you can fill in the **Active Code**. This product can be tried **eight times for free**.

After executing the above 3 steps, we need to add a windows timer program to execute the program regularly. In this part, you can search the Internet for how to write a bat script and how to set the windows timer program.

After the program is successfully executed, if there are failed jobs in your cluster, an email will be sent to the recipient's mailbox. If you check the option **AttachLogFile**, there will be an execution log of the failed jobs in the attachment.
![pic11](https://github.com/mxxt/my_image/blob/master/sense_conf_12.jpeg?raw=true)

Noted: After the first execution of this program, a program execution log folder and a failed job log folder are created. The default setting is to keep only the execution log files for the last 7 days and the failed job log files for the last 15 days.
