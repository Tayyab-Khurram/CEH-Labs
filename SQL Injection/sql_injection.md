 ## 𝗪𝗵𝗲𝗻 𝗜𝗻𝗽𝘂𝘁𝘀 𝗧𝘂𝗿𝗻 𝗗𝗲𝗮𝗱𝗹𝘆, 𝗧𝗵𝗶𝘀 𝗜𝘀 𝗪𝗵𝗮𝘁 𝗛𝗮𝗽𝗽𝗲𝗻𝘀 💀

SQL Injection:  
● A nightmare for developers.  
● A dream for penetration testers.  

Recently, I conducted an in-depth SQL injection assessment on  
𝗣𝗼𝗿𝘁𝗦𝘄𝗶𝗴𝗴𝗲𝗿'𝘀 𝗪𝗲𝗯 𝗦𝗲𝗰𝘂𝗿𝗶𝘁𝘆 𝗔𝗰𝗮𝗱𝗲𝗺𝘆 𝗟𝗮𝗯𝘀 to explore various methods of exploiting SQL vulnerabilities in web applications.


![Image](https://github.com/user-attachments/assets/ebfeed90-5691-4ae1-91d4-167c96fa9de8)
![Image](https://github.com/user-attachments/assets/cea0556e-181f-4fcb-a31c-fe0a52d549ce)
![Image](https://github.com/user-attachments/assets/105a66dc-5ef4-4d3c-a30e-9552c53f32bc)
![Image](https://github.com/user-attachments/assets/8643b36b-22b9-4d30-bf5e-d8d474e8bfc8)
![Image](https://github.com/user-attachments/assets/d656a6d9-aa72-436f-9abc-b4bb1375d462)
![Image](https://github.com/user-attachments/assets/0c7d3213-c3fd-496e-9847-0d6af6c96594)
![Image](https://github.com/user-attachments/assets/ace2831d-b97e-40a9-82b4-9b057525730f)
![Image](https://github.com/user-attachments/assets/70edf4b3-4d51-49c7-a250-2753c25c95b1)
![Image](https://github.com/user-attachments/assets/8cf83e65-d6b6-49d8-8716-2566081a7add)
![Image](https://github.com/user-attachments/assets/a59a8b1d-b94c-4349-a5aa-f27fa3deabf6)

### Here are the key techniques I successfully implemented:

► Accessing hidden records  
► Retrieving sensitive data  
► Login bypass  
► Identifying column data types  
► Determining the database version  
► Determining the number of columns  

𝗣𝗿𝗲𝘃𝗲𝗻𝘁𝗮𝘁𝗶𝘃𝗲 𝗠𝗲𝗮𝘀𝘂𝗿𝗲𝘀 𝗔𝗴𝗮𝗶𝗻𝘀𝘁 𝗦𝗤𝗟 𝗜𝗻𝗷𝗲𝗰𝘁𝗶𝗼𝗻 𝗔𝘁𝘁𝗮𝗰𝗸𝘀:

1. 𝗣𝗮𝗿𝗮𝗺𝗲𝘁𝗲𝗿𝗶𝘇𝗲𝗱 𝗤𝘂𝗲𝗿𝗶𝗲𝘀/𝗣𝗿𝗲𝗽𝗮𝗿𝗲𝗱 𝗦𝘁𝗮𝘁𝗲𝗺𝗲𝗻𝘁𝘀: Always use parameterized queries to separate SQL code from user input.
2. 𝗜𝗻𝗽𝘂𝘁 𝗩𝗮𝗹𝗶𝗱𝗮𝘁𝗶𝗼𝗻: Validate and sanitize all user inputs to prevent malicious code execution.
3. 𝗦𝘁𝗼𝗿𝗲𝗱 𝗣𝗿𝗼𝗰𝗲𝗱𝘂𝗿𝗲𝘀: Use stored procedures to reduce the risk of direct user input in SQL commands.
4. 𝗘𝗿𝗿𝗼𝗿 𝗛𝗮𝗻𝗱𝗹𝗶𝗻𝗴: Avoid exposing detailed error messages, as they may reveal clues about the database structure.
5. 𝗟𝗶𝗺𝗶𝘁 𝗗𝗮𝘁𝗮𝗯𝗮𝘀𝗲 𝗣𝗿𝗶𝘃𝗶𝗹𝗲𝗴𝗲𝘀: Assign the least privileges necessary to the database user account interacting with the application.
6. 𝗪𝗲𝗯 𝗔𝗽𝗽𝗹𝗶𝗰𝗮𝘁𝗶𝗼𝗻 𝗙𝗶𝗿𝗲𝘄𝗮𝗹𝗹𝘀 (𝗪𝗔𝗙𝘀): Use WAFs to detect and block malicious traffic.

