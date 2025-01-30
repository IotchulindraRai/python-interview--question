<!-- markdown-toc start - Don't edit this section. Run M-x markdown-toc-generate-toc again -->
* [Python Basics](#python-basics)
    * 1. File Operations
        * **1.1. There's a jsonline format file file.txt with a size of about 10K.**
            * **Answer:** A jsonline file is a text file where each line is a valid JSON object. You can use Python's `json` module to parse the file.
        * **1.2. Complete the missing code?**
            * **Answer:** Please provide the code snippet, and I can help complete it.
    * 2. Modules and Packages
        * **2.1. Input a date and determine the day of the year for that date?**
            * **Answer:** 
                ```python
                from datetime import datetime
                date_input = input("Enter a date (YYYY-MM-DD): ")
                date_obj = datetime.strptime(date_input, "%Y-%m-%d")
                day_of_year = date_obj.timetuple().tm_yday
                print(f"Day of the year: {day_of_year}")
                ```
        * **2.2. Shuffle a sorted list object alist?**
            * **Answer:**
                ```python
                import random
                alist = [1, 2, 3, 4, 5]
                random.shuffle(alist)
                print(alist)
                ```
    * 3. Data Types
        * **3.1. Given the dictionary d={'a':24, 'g':52, 'i':12, 'k':33}, please sort by the value.**
            * **Answer:**
                ```python
                d = {'a':24, 'g':52, 'i':12, 'k':33}
                sorted_d = dict(sorted(d.items(), key=lambda item: item[1]))
                print(sorted_d)
                ```
        * **3.2. Dictionary comprehension?**
            * **Answer:** Dictionary comprehension allows creating dictionaries in a single line using a syntax like:
                ```python
                d = {key: value for key, value in iterable}
                ```
        * **3.3. Reverse the string "aStr"?**
            * **Answer:** 
                ```python
                aStr = "Hello"
                reversed_str = aStr[::-1]
                print(reversed_str)
                ```
        * **3.4. Convert the string "k:1|k1:2|k2:3|k3:4" into a dictionary: {k:1, k1:2, k2:3, k3:4}.**
            * **Answer:**
                ```python
                s = "k:1|k1:2|k2:3|k3:4"
                result = dict(item.split(":") for item in s.split("|"))
                print(result)
                ```
        * **3.5. Sort elements in alist by age in descending order.**
            * **Answer:** 
                ```python
                alist = [{'name': 'Alice', 'age': 30}, {'name': 'Bob', 'age': 25}]
                sorted_list = sorted(alist, key=lambda x: x['age'], reverse=True)
                print(sorted_list)
                ```
        * **3.6. What will be the output of the following code?**
            * **Answer:** Please provide the code snippet, and I'll explain the output.
        * **3.7. Write a list comprehension to generate an arithmetic sequence with a common difference of 11.**
            * **Answer:**
                ```python
                sequence = [x for x in range(0, 101, 11)]
                print(sequence)
                ```
        * **3.8. Given two lists, how do you find the common and different elements?**
            * **Answer:**
                ```python
                list1 = [1, 2, 3, 4]
                list2 = [3, 4, 5, 6]
                common = list(set(list1) & set(list2))
                different = list(set(list1) ^ set(list2))
                print(f"Common: {common}, Different: {different}")
                ```
        * **3.9. Write Python code to remove duplicate elements from a list.**
            * **Answer:**
                ```python
                my_list = [1, 2, 2, 3, 4, 4]
                unique_list = list(set(my_list))
                print(unique_list)
                ```
        * **3.10. Given two lists A and B, how to find common and different elements?**
            * **Answer:** See answer for **3.8**.
    * 4. Company Interview Questions
        * **4.1. Difference between Python new-style class and classic class?**
            * **Answer:** New-style classes are subclasses of `object`, while classic classes are not. New-style classes support descriptors, metaclasses, etc.
        * **4.2. How many built-in data structures are there in Python?**
            * **Answer:** Python has several built-in data structures, including lists, tuples, sets, dictionaries, and strings.
        * **4.3. How do you implement the Singleton pattern in Python? Provide two methods.**
            * **Answer:**
                1. Using a class variable to hold the instance.
                2. Using a metaclass to enforce a single instance.
        * **4.4. Reverse an integer, e.g., -123 → -321, implemented in Python.**
            * **Answer:**
                ```python
                def reverse_int(n):
                    sign = -1 if n < 0 else 1
                    n = abs(n)
                    reversed_n = int(str(n)[::-1])
                    return sign * reversed_n
                print(reverse_int(-123))
                ```
        * **4.5. Design a function to traverse directories and subdirectories to grab .pyc files.**
            * **Answer:**
                ```python
                import os
                def find_pyc_files(directory):
                    pyc_files = []
                    for root, dirs, files in os.walk(directory):
                        for file in files:
                            if file.endswith('.pyc'):
                                pyc_files.append(os.path.join(root, file))
                    return pyc_files
                ```
        * **4.6. Write a one-liner to calculate the sum of numbers from 1 to 100.**
            * **Answer:**
                ```python
                print(sum(range(1, 101)))
                ```
        * **4.7. Correct way to remove elements from a list while iterating in Python.**
            * **Answer:** Use list comprehension or iterate in reverse order.
                ```python
                my_list = [1, 2, 3, 4]
                my_list = [x for x in my_list if x != 2]
                ```
        * **4.8. String manipulation problems.**
            * **Answer:** Please provide the specific question.
        * **4.9. Mutable and Immutable types in Python.**
            * **Answer:** Lists, sets, and dictionaries are mutable, while strings, tuples, and integers are immutable.
        * **4.10. What is the difference between is and ==?**
            * **Answer:** `is` checks for identity (whether two references point to the same object), while `==` checks for equality (whether the values are the same).
        * **4.11. Find all odd numbers in a list and construct a new list.**
            * **Answer:**
                ```python
                numbers = [1, 2, 3, 4, 5]
                odd_numbers = [num for num in numbers if num % 2 != 0]
                print(odd_numbers)
                ```
        * **4.12. Write one line of Python code to calculate 1 + 2 + 3 + ... + 10248.**
            * **Answer:** 
                ```python
                print(sum(range(1, 10249)))
                ```
        * **4.13. What is variable scope in Python? (Variable lookup order)**
            * **Answer:** Variable scope refers to where a variable is accessible. The lookup order is: Local -> Enclosing -> Global -> Built-in.
        * **4.14. Convert the string "123" into an integer without using built-in APIs like int().**
            * **Answer:**
                ```python
                string = "123"
                result = sum([int(digit) * (10 ** i) for i, digit in enumerate(reversed(string))])
                print(result)
                ```
        * **4.15. Given an array of integers.**
            * **Answer:** Please provide the complete question.
        * **4.16. Python code to remove duplicate elements from a list.**
            * **Answer:** See answer for **3.9**.
        * **4.17. Find the top 10 most frequent words in a text.**
            * **Answer:** Use the `collections.Counter` to count words and retrieve the top 10.
                ```python
                from collections import Counter
                text = "your text here"
                word_counts = Counter(text.split())
                print(word_counts.most_common(10))
                ```
        * **4.18. Write a function that satisfies the following condition.**
            * **Answer:** Please provide the condition to be satisfied.
        * **4.19. Use a single list comprehension to generate a new list.**
            * **Answer:** Please provide the full list generation requirement.
        * **4.20. Design a function that checks whether a given string is a valid email address.**
            * **Answer:** You can use regex to validate the email.
                ```python
                import re
                def is_valid_email(email):
                    pattern = r"^[a-zA-Z0-9_.+-]+@[a-zA-Z0-9-]+\.[a-zA-Z0-9-.]+$"
                    return bool(re.match(pattern, email))
                ```

<!-- markdown-toc start - Don't edit this section. Run M-x markdown-toc-generate-toc again -->
* Web Crawling
    * **1.1. List at least three popular large databases currently.**
      - **Answer:** 
        - MySQL
        - MongoDB
        - PostgreSQL
    * **1.2. List the Python network crawling packages you have used.**
      - **Answer:** 
        - Requests
        - urllib
        - Selenium
        - Scrapy
    * **1.3. List the Python network crawling data parsing packages you have used.**
      - **Answer:** 
        - BeautifulSoup
        - lxml
        - PyQuery
    * **1.4. After crawling data, which database do you use to store the data, and why?**
      - **Answer:** 
        - I typically use **MySQL** for structured data that requires relational storage. For large, unstructured datasets, **MongoDB** is preferred due to its flexibility with document storage. **Redis** can be used for caching or storing temporary data.
    * **1.5. What web crawling frameworks or modules have you used? What are the pros and cons?**
      - **Answer:** 
        - **Scrapy**: Efficient, highly extensible, supports asynchronous scraping. However, it has a steeper learning curve.
        - **Selenium**: Useful for crawling dynamic websites. It is slower compared to Scrapy but works well with JavaScript-heavy pages.
    * **1.6. Is it better to use multiprocessing or multithreading for writing a crawler?**
      - **Answer:** 
        - **Multiprocessing** is usually better for CPU-bound tasks since it runs processes in separate memory spaces. **Multithreading** is preferable for I/O-bound tasks like web scraping, where the task waits for external responses.
    * **1.7. Common anti-crawling methods and countermeasures?**
      - **Answer:** 
        - **Rate limiting**: Implement delays or use proxies to avoid getting blocked.
        - **CAPTCHA**: Use CAPTCHA-solving tools like 2Captcha or bypass with Selenium for automated solving.
        - **IP blocking**: Use rotating proxies or VPNs to change IP addresses.
    * **1.8. Which parsers are most commonly used for parsing web pages?**
      - **Answer:** 
        - **BeautifulSoup**
        - **lxml**
        - **html5lib**
    * **1.9. How to solve login pages that limit IPs, cookies, and sessions simultaneously?**
      - **Answer:** 
        - Use rotating IP proxies, session management techniques, and ensure the usage of valid cookies. In cases of highly restricted login systems, it may be necessary to use a headless browser like **Selenium** to simulate a real user login process.
    * **1.10. How do you handle CAPTCHA solutions?**
      - **Answer:** 
        - Use CAPTCHA-solving services like **2Captcha**, **Anti-Captcha**, or use machine learning techniques to recognize CAPTCHAs if you have a high volume.
    * **1.11. Most commonly used databases, and your understanding of them?**
      - **Answer:** 
        - **MySQL**: A relational database that uses SQL for querying data.
        - **MongoDB**: A NoSQL database that uses collections and documents to store data, suitable for unstructured or semi-structured data.
        - **Redis**: An in-memory data store, used for caching and sessions.
    * **1.12. What crawling middlewares have you written?**
      - **Answer:** 
        - I have written middlewares for proxy rotation, handling retries, and managing user-agent spoofing to avoid detection.
    * **1.13. How to crack the "Geetest" sliding CAPTCHA?**
      - **Answer:** 
        - Use **Selenium** combined with image recognition libraries to solve or bypass the Geetest CAPTCHA.
    * **1.14. How often do you crawl, and how is the crawled data stored?**
      - **Answer:** 
        - Crawling frequency depends on the website's content updates. For example, news websites may be crawled every hour, while product websites may be updated once a day. Data is typically stored in databases like MySQL or MongoDB.
    * **1.15. How do you handle expired cookies?**
      - **Answer:** 
        - Regularly refresh cookies by logging in again if necessary, and ensure the cookies are valid before sending requests.
    * **1.16. How do you handle dynamic loading when high timeliness is required?**
      - **Answer:** 
        - Use **Selenium** with proper waits or use **Scrapy**'s asynchronous features to scrape the content as it loads dynamically.
    * **1.17. What are the advantages and disadvantages of HTTPS?**
      - **Answer:** 
        - **Advantages**: Secure communication, encrypted data transmission, and authenticity verification.
        - **Disadvantages**: Increased computational overhead, slower speeds compared to HTTP.
    * **1.18. How does HTTPS ensure secure data transmission?**
      - **Answer:** 
        - HTTPS uses SSL/TLS protocols to encrypt the data transferred between the client and the server, ensuring that data cannot be intercepted or tampered with.
    * **1.19. What are TTL, MSL, and RTT?**
      - **Answer:** 
        - **TTL (Time to Live)**: Determines the lifespan of a packet in a network before it is discarded.
        - **MSL (Maximum Segment Lifetime)**: The maximum time a TCP segment can remain in the network.
        - **RTT (Round Trip Time)**: The time it takes for a signal to travel from the source to the destination and back.
    * **1.20. What do you know about Selenium and PhantomJS?**
      - **Answer:** 
        - **Selenium**: A tool for automating web browsers, useful for scraping dynamic content.
        - **PhantomJS**: A headless browser that can be controlled via scripts, useful for scraping without opening a visible browser.
    * **1.21. How do you use proxies?**
      - **Answer:** 
        - Use rotating proxies to avoid detection and blocking. Services like **ScraperAPI**, **ProxyMesh**, or custom proxy rotations are commonly used.
    * **1.22. How do you store data in databases (e.g., Redis, MySQL)?**
      - **Answer:** 
        - Store crawled data in a structured format in **MySQL** or use **Redis** for temporary data storage.
    * **1.23. How do you monitor the status of your crawler?**
      - **Answer:** 
        - Use logging and alerting systems to monitor errors, success rates, and completion of tasks. Tools like **Celery** or **Scrapy Cloud** can provide task monitoring.
    * **1.24. Describe the mechanism of the Scrapy framework.**
      - **Answer:** 
        - **Scrapy** works by sending requests to the target website, processing the responses through spider functions, and saving the data into a database or file using pipelines.
    * **1.25. What is your understanding of Scrapy?**
      - **Answer:** 
        - **Scrapy** is an open-source framework that facilitates the scraping of websites by providing robust support for concurrency, scraping rules, data pipelines, and exporting scraped data.
    * **1.26. How do you send a POST request in Scrapy (write the code)?**
      - **Answer:** 
        ```python
        def start_requests(self):
            yield scrapy.FormRequest(
                'http://example.com/login', 
                formdata={'username': 'user', 'password': 'pass'},
                callback=self.parse_after_login
            )
        ```
    * **1.27. How do you monitor the status of your crawler?**
      - **Answer:** 
        - Use tools like **Scrapy's built-in statistics** or integrate with third-party systems like **Elasticsearch** or **Prometheus** for real-time monitoring.
    * **1.28. How do you determine if a website has been updated?**
      - **Answer:** 
        - Track specific content changes or use webhooks that notify when content is updated.
    * **1.29. How do you bypass hotlinking protection for image and video crawling?**
      - **Answer:** 
        - Use **random user-agents** and **proxy rotation** to simulate real users.
    * **1.30. How much data do you crawl? How often do you crawl?**
      - **Answer:** 
        - The amount of data crawled depends on the project. Typically, I crawl several GB of data per day for large websites, adjusting frequency based on the website's update cycle.
    * **1.31. What database do you use to store crawled data? Did you deploy it yourself? How did you deploy it?**
      - **Answer:** 
        - I store data in **MySQL** for structured data and deploy the database on cloud services like **AWS RDS** for scalability and management.
    * **1.32. Incremental crawling.**
      - **Answer:** 
        - **Incremental crawling** ensures that only new or updated data is scraped by keeping track of previously crawled data, often by using timestamps or hashes.
    * **1.33. How do you remove duplicates from crawled data? Explain the algorithm used in Scrapy.**
      - **Answer:** 
        - Scrapy uses a **deduplication filter** in its `dupefilter` system that stores URLs that have already been scraped, ensuring each URL is processed only once.
    * **1.34. Advantages and disadvantages of Scrapy?**
      - **Answer:** 
        - **Advantages**: Fast, flexible, supports asynchronous processing, and integrates well with many databases.
        - **Disadvantages**: Steep learning curve for beginners and can be overkill for small projects.
    * **1.35. How do you set crawl depth in Scrapy?**
      - **Answer:** 
        - Set the **DEPTH_LIMIT** setting in Scrapy to control the maximum depth of the crawl.
    * **1.36. What is the difference between Scrapy and Scrapy-Redis? Why use Redis?**
      - **Answer:** 
        - **Scrapy-Redis** is an extension of Scrapy that allows for distributed crawling using Redis. Redis stores crawled URLs and task queues, enabling parallel crawlers to work efficiently.
    * **1.37. What problems does distributed crawling mainly solve?**
      - **Answer:** 
        - Distributed crawling solves scalability issues, increases crawl speed, and allows for the handling of large-scale web scraping tasks across multiple machines.
    * **1.38. What is distributed storage?**
      - **Answer:** 
        - **Distributed storage** refers to storing data across multiple physical machines to improve scalability, redundancy, and availability. Examples include **HDFS** and **Amazon S3**.
    * **1.39. What distributed crawling solutions do you know?**
      - **Answer:** 
        - Solutions like **Scrapy-Redis**, **Apache Nutch**, and **Heritrix** support distributed web crawling.
    * **1.40. Have you worked with any distributed crawlers other than Scrapy-Redis?**
      - **Answer:** 
        - Yes, I have worked with **Apache Nutch** and **Heritrix** for large-scale web crawling.
        - 
<!-- markdown-toc end -->
<!-- markdown-toc start - Don't edit this section. Run M-x markdown-toc-generate-toc again -->
* Database
    * 1. MySQL
        * 1.1. **Primary key, superkey, candidate key, foreign key**
            * **Primary key:** A primary key uniquely identifies each record in a table. It must contain unique values and cannot have NULLs.
            * **Superkey:** A superkey is a set of one or more attributes that can uniquely identify a record. A primary key is a superkey, but not all superkeys are primary keys.
            * **Candidate key:** A candidate key is a minimal superkey, i.e., it uniquely identifies a record but does not contain any unnecessary attributes.
            * **Foreign key:** A foreign key is a column (or set of columns) that links one table to another, establishing a relationship between the two.
        * 1.2. **Purpose of views, and can views be modified?**
            * **Purpose of views:** Views are used to simplify complex queries, provide a layer of abstraction, and improve security by limiting access to specific data in a table.
            * **Can views be modified?** Yes, views can be modified if they are updatable views. However, not all views are updatable, especially if they involve joins, aggregates, or non-trivial calculations.
        * 1.3. **Difference between DROP, DELETE, and TRUNCATE**
            * **DROP:** Removes a table or database completely, including its structure and data.
            * **DELETE:** Removes records from a table based on a condition, and it can be rolled back if wrapped in a transaction.
            * **TRUNCATE:** Removes all records from a table, but the table structure remains. It cannot be rolled back in some databases.
        * 1.4. **Working principles and types of indexes**
            * Indexes are used to speed up query processing by providing a fast lookup for data in a table. They can be based on one or more columns.
            * **Types of indexes:** Single-column index, composite index, unique index, full-text index, and spatial index.
        * 1.5. **Types of joins**
            * **INNER JOIN:** Returns records that have matching values in both tables.
            * **LEFT JOIN (or LEFT OUTER JOIN):** Returns all records from the left table, and the matched records from the right table. Unmatched rows in the right table will have NULL values.
            * **RIGHT JOIN (or RIGHT OUTER JOIN):** Returns all records from the right table, and the matched records from the left table. Unmatched rows in the left table will have NULL values.
            * **FULL JOIN (or FULL OUTER JOIN):** Returns records when there is a match in one of the tables.
            * **CROSS JOIN:** Returns the Cartesian product of two tables.
        * 1.6. **Ideas for database optimization**
            * Use indexing to speed up queries.
            * Normalize the database to reduce redundancy.
            * Denormalize in certain cases where performance is crucial.
            * Optimize queries by avoiding unnecessary subqueries or joins.
            * Use database partitioning to distribute data across multiple locations.
        * 1.7. **Difference between stored procedures and triggers**
            * **Stored procedure:** A stored procedure is a precompiled collection of SQL statements that can be executed on demand. It can be called explicitly by the user.
            * **Trigger:** A trigger is a set of actions automatically invoked by the database in response to certain events (INSERT, UPDATE, DELETE).
        * 1.8. **What are pessimistic and optimistic locks?**
            * **Pessimistic lock:** Locks a resource as soon as it is accessed, preventing others from modifying it until the lock is released.
            * **Optimistic lock:** Assumes that no conflicts will occur and allows multiple transactions to access the same resource. If a conflict occurs, it handles it when the changes are committed.
        * 1.9. **Which MySQL engines do you commonly use? What are the differences between them?**
            * **InnoDB:** The default storage engine in MySQL. It supports transactions, foreign keys, and ACID compliance.
            * **MyISAM:** An older storage engine, faster for read-heavy workloads but does not support transactions or foreign keys.
            * **MEMORY:** Stores data in memory for fast access but is volatile.
            * **ARCHIVE:** Optimized for storing large amounts of data with minimal overhead.
    * 2. Redis
        * 2.1. **How do you solve Redis downtime?**
            * To solve Redis downtime, you can implement Redis replication with a master-slave setup and enable automatic failover using Redis Sentinel.
        * 2.2. **Difference between Redis and Memcached, and use cases**
            * **Redis:** An in-memory data store that supports complex data types (strings, hashes, lists, sets). It is used for caching, session storage, pub/sub systems, and queues.
            * **Memcached:** A high-performance, distributed memory object caching system, mainly used for caching simple key-value pairs.
        * 2.3. **Redis cluster solutions, and available options**
            * Redis supports clustering to distribute data across multiple nodes. Redis Cluster provides automatic sharding and high availability.
        * 2.4. **How does Redis's eviction process work?**
            * Redis uses an eviction policy to remove keys from memory when it reaches its memory limit. Common eviction policies include LRU (Least Recently Used), LFU (Least Frequently Used), and random eviction.
    * 3. MongoDB
        * 3.1. **Command for updating multiple records in MongoDB?**
            * Use `db.collection.updateMany(filter, update)` to update multiple documents that match the filter.
        * 3.2. **When will MongoDB scale to multiple shards?**
            * MongoDB scales to multiple shards when data grows too large to be stored on a single server, or when read/write operations become a bottleneck.
* Testing
    * 1. **Purpose of writing test plans**
        * Test plans define the scope, approach, resources, and schedule for testing activities. They provide a systematic approach to ensure that all functionalities are tested thoroughly.
    * 2. **Testing keyword triggering modules**
        * A keyword triggering module executes test cases based on specific input or actions that trigger the test process automatically.
    * 3. **Common online test question repositories**
        * Websites like LeetCode, HackerRank, GeeksforGeeks, and Stack Overflow contain a vast repository of programming and testing-related questions.
    * 4. **Tasks of testing personnel in the software development process**
        * Testing personnel are responsible for creating test cases, executing tests, reporting defects, and ensuring the quality of software.
    * 5. **What information does a software bug report include?**
        * A bug report typically includes the bug description, steps to reproduce, expected and actual results, environment details, and any logs or screenshots.
    * 6. **Pros and cons of black-box testing and white-box testing**
        * **Black-box testing:** Focuses on functionality without knowledge of internal code. Pros: easy to use, user-centric. Cons: limited coverage.
        * **White-box testing:** Involves testing internal structures and code. Pros: thorough and detailed. Cons: requires coding knowledge and is time-consuming.
    * 7. **List of software testing types you know (at least 5)**
        * Unit testing, Integration testing, System testing, Acceptance testing, Regression testing.
    * 8. **Difference between Alpha and Beta testing**
        * **Alpha testing:** Done by the internal team before releasing the software to external users.
        * **Beta testing:** Done by a limited number of external users to gather feedback and identify issues before the official release.
    * 9. **Examples of bugs and what a bug report should contain**
        * **Examples of bugs:** UI layout issues, functionality errors, performance problems.
        * A bug report should contain: title, description, steps to reproduce, expected result, actual result, environment, screenshots, and logs.
* Data Structures
    * 1.1. **Find the number in an array that appears more than half of the time – Python version**
        ```python
        def majority_element(nums):
            count = {}
            for num in nums:
                count[num] = count.get(num, 0) + 1
                if count[num] > len(nums) // 2:
                    return num
        ```
    * 1.2. **Find prime numbers up to 100**
        ```python
        def primes_up_to_100():
            primes = []
            for num in range(2, 101):
                if all(num % i != 0 for i in range(2, int(num ** 0.5) + 1)):
                    primes.append(num)
            return primes
        ```
    * 1.3. **Longest substring without repeating characters – Python implementation**
        ```python
        def length_of_longest_substring(s):
            chars = {}
            left = 0
            max_len = 0
            for right in range(len(s)):
                if s[right] in chars:
                    left = max(left, chars[s[right]] + 1)
                chars[s[right]] = right
                max_len = max(max_len, right - left + 1)
            return max_len
        ```
    * 1.4. **How to get 3 liters of water using two 5/6 liter jugs**
        * Fill one jug, then pour it into the other jug until it's full. Continue this process until you have 3 liters in one jug.
    * 1.5. **What is MD5 encryption and its characteristics?**
        * MD5 (Message Digest Algorithm 5) is a cryptographic hash function that produces a 128-bit hash value. It's fast but not secure for cryptographic purposes due to vulnerabilities.
    * 1.6. **What is symmetric and asymmetric encryption?**
        * **Symmetric encryption:** Uses the same key for encryption and decryption.
        * **Asymmetric encryption:** Uses a public key for encryption and a private key for decryption.
    * 1.7. **Bubble sort algorithm**
        * Bubble sort repeatedly steps through the list, compares adjacent items, and swaps them if they are in the wrong order.
    * 1.8. **Quick sort algorithm**
        * Quick sort works by selecting a pivot element and partitioning the array into two subarrays, recursively sorting them.
    * 1.9. **How to detect cycles in a singly linked list?**
        * Use two pointers: one moves two steps at a time, and the other moves one step at a time. If they meet, a cycle exists.
    * 1.10. **What sorting algorithms do you know?**
        * Bubble sort, Merge sort, Quick sort, Insertion sort, Selection sort, Heap sort.
    * 1.11. **Fibonacci sequence**
        * The Fibonacci sequence is a series where each number is the sum of the two preceding ones.
    * 1.12. **How to reverse a singly linked list?**
        * Iterate through the list, reversing the direction of each link until the entire list is reversed.
    * 1.13. **Frog jump problem**
        * The frog can jump a maximum distance of k steps at a time. Use dynamic programming to calculate the minimum cost for each step.
    * 1.14. **Two sum problem**
        * Given an array of integers and a target sum, find two numbers that add up to the target. Use a hash map to store the difference.
    * 1.15. **Search in rotated sorted array**
        * Use binary search to find the pivot point and determine which part of the array is sorted. Perform binary search on the sorted part.
    * 1.16. **Implement a stack in Python**
        ```python
        class Stack:
            def __init__(self):
                self.stack = []
            def push(self, value):
                self.stack.append(value)
            def pop(self):
                return self.stack.pop() if self.stack else None
            def peek(self):
                return self.stack[-1] if self.stack else None
        ```
    * 1.17. **Write a binary search function**
        ```python
        def binary_search(arr, target):
            left, right = 0, len(arr) - 1
            while left <= right:
                mid = (left + right) // 2
                if arr[mid] == target:
                    return mid
                elif arr[mid] < target:
                    left = mid + 1
                else:
                    right = mid - 1
            return -1
        ```
    * 1.18. **What is the time complexity of 'in' operation in a set, and why?**
        * The time complexity is O(1) on average because sets use a hash table for storage.
    * 1.19. **Sort a list with n integers between 0 and 1000**
        ```python
        def counting_sort(arr):
            count = [0] * 1001
            for num in arr:
                count[num] += 1
            result = []
            for i, freq in enumerate(count):
                result.extend([i] * freq)
            return result
        ```
    * 1.20. **Object-oriented programming, implementing a new class using composition and inheritance**
        ```python
        class Engine:
            def start(self):
                print("Engine started")
        
        class Car:
            def __init__(self, engine):
                self.engine = engine
            def drive(self):
                self.engine.start()
                print("Car is driving")
        ```
* Artificial Intelligence
    * 1.1. **Find high-frequency words in a 1GB file**
        * You can use Python with the `collections.Counter` class to efficiently process large files and count word frequencies.
    * 1.2. **Count high-frequency words in a file with about 10,000 lines**
        * Use `Counter` from the `collections` module to count the frequency of words and identify the most frequent ones.
    * 1.3. **How to find the most repeated item in massive data?**
        * Use a streaming algorithm like the **Misra-Gries algorithm** or **Count-Min Sketch** for approximate results in large datasets.
    * 1.4. **How to check if data exists in large datasets?**
        * Use hash-based data structures (e.g., hash sets) or approximate algorithms like **Bloom Filters** to check for the existence of data efficiently.

<!-- markdown-toc end -->


    *   7、系统编程
        *   7.1、进程总结
        *   7.2、谈谈你对多进程，多线程，以及协程的理解，项目是否用？
        *   7.3、Python异步使用场景有那些？
        *   7.4、多线程共同操作同一个数据互斥锁同步？
        *   7.5、什么是多线程竞争？
        *   7.6、请介绍一下Python的线程同步？
        *   7.7、解释一下什么是锁，有哪几种锁?
        *   7.8、什么是死锁呢？
        *   7.9、多线程交互访问数据，如果访问到了就不访问了
        *   7.10、什么是线程安全，什么是互斥锁？
        *   7.11、说说下面几个概念：同步，异步，阻塞，非阻塞?
        *   7.12、什么是僵尸进程和孤儿进程？怎么避免僵尸进程?
        *   7.13、Python中的进程与线程的使用场景?
        *   7.14、线程是并发还是并行，进程是并发还是并行？
        *   7.15、并行（parallel）和并发（concurrency）？
        *   7.16、IO密集型和CPU密集型区别？
    *   8、网络编程
        *   8.1、怎么实现强行关闭客户端和服务器之间的连接?
        *   8.2、简述TCP和UDP的区别以及优缺点?
        *   8.3、简述浏览器通过WSGI请求动态资源的过程?
        *   8.4、描述用浏览器访问www.baidu.com的过程
        *   8.5、Post和Get请求的区别?
        *   8.6、cookie 和session 的区别？
        *   8.7、列出你知道的HTTP协议的状态码，说出表示什么意思？
        *   8.8、请简单说一下三次握手和四次挥手？
        *   8.9、说一下什么是tcp的2MSL？
        *   8.10、为什么客户端在TIME-WAIT状态必须等待2MSL的时间？
        *   8.11、说说HTTP和HTTPS区别？
        *   8.12、谈一下HTTP协议以及协议头部中表示数据类型的字段？
        *   8.13、HTTP请求方法都有什么？
        *   8.14、使用Socket套接字需要传入哪些参数 ？
        *   8.15、HTTP常见请求头？
        *   8.16、七层模型？
        *   8.17、url的形式？
    *   三、Web
        *   1、Flask
            *   1.1、对Flask蓝图(Blueprint)的理解？
            *   1.2、Flask和Django路由映射的区别？
        *   Django
            *   2.1、什么是wsgi,uwsgi,uWSGI？
            *   2.3、CORS和CSRF的区别？
            *   2.4、Session、Cookie、JWT的理解 
            *   2.5、简述Django请求生命周期 
            *   2.6、什么是wsgi,uwsgi,uWSGI？
            *   2.7、Django 、Flask、Tornado的对比
            *   2.8、用的restframework完成api发送时间时区
            *   2.9、nginx,tomcat,apache 都是什么?
            *   2.10、请给出你熟悉关系数据库范式有那些，有什么作用
            *   2.11、简述QQ登陆过程
            *   2.12、post和get 的区别？
            *   2.13、项目中日志的作用
            *   2.14、django中间件的使用？
            *   2.15、谈一下你对uWSGI和 nginx的理解？
            *   2.16、Python中三大框架各自的应用场景？
            *   2.17、有过部署经验？用的什么技术？可以满足多少压力？
            *   2.18、Django中哪里用到了线程?哪里用到了协程?哪里用到了进程？
            *   2.19、有用过Django REST framework 吗？
            *   2.20、对cookie与session的了解？他们能单独用吗？
        *   爬虫
            *   1.1、试列出至少三种目前流行的大型数据库
            *   1.2、列举您使用过的Python网络爬虫所用到的网络数据包?
            *   1.3、列举您使用过的Python网络爬虫所用到的解析数据包？
            *   1.4、爬取数据后使用哪个数据库存储数据的，为什么？
            *   1.5、你用过的爬虫框架或者模块有哪些？优缺点？
            *   1.6、写爬虫是用多进程好？还是多线程好？
            *   1.7、常见的反爬虫和应对方法？
            *   1.8、解析网页的解析器使用最多的是哪几个?
            *   1.9、需要登录的网页，如何解决同时限制ip，cookie,session
            *   1.10、验证码的解决?
            *   1.11、使用最多的数据库，对他们的理解？
            *   1.12、编写过哪些爬虫中间件？
            *   1.13、“极验”滑动验证码如何破解？
            *   1.14、爬虫多久爬一次，爬下来的数据是怎么存储？
            *   1.15、cookie过期的处理问题？
            *   1.16、动态加载又对及时性要求很高怎么处理？
            *   1.17、HTTPS有什么优点和缺点？
            *   1.18、HTTPS是如何实现安全传输数据的？
            *   1.19、TTL，MSL，RTT各是什么？
            *   1.20、谈一谈你对Selenium和PhantomJS了解
            *   1.21、平常怎么使用代理的 ？
            *   1.22、存放在数据库(redis、mysql等)。
            *   1.23、怎么监控爬虫的状态?
            *   1.24、描述下scrapy框架运行的机制？
            *   1.25、谈谈你对Scrapy的理解？
            *   1.26、怎么样让 scrapy 框架发送一个 post 请求（具体写出来）
            *   1.27、怎么监控爬虫的状态 ？
            *   1.28、怎么判断网站是否更新？
            *   1.29、图片、视频爬取怎么绕过防盗连接
            *   1.30、你爬出来的数据量大概有多大？大概多长时间爬一次？
            *   1.31、用什么数据库存爬下来的数据？部署是你做的吗？怎么部署？
            *   1.32、增量爬取
            *   1.33、爬取下来的数据如何去重，说一下scrapy的具体的算法依据。
            *   1.34、Scrapy的优缺点?
            *   1.35、怎么设置爬取深度？
            *   1.36、scrapy和scrapy-redis有什么区别？为什么选择redis数据库？
            *   1.37、分布式爬虫主要解决什么问题？
            *   1.38、什么是分布式存储？
            *   1.39、你所知道的分布式爬虫方案有哪些？
            *   1.40、scrapy-redis，有做过其他的分布式爬虫吗？
*   五、数据库
    *   1、MySQL
        *   1.1、主键 超键 候选键 外键
        *   1.2、视图的作用，视图可以更改么？
        *   1.3、drop,delete与truncate的区别
        *   1.4、索引的工作原理及其种类
        *   1.5、连接的种类
        *   1.6、数据库优化的思路
        *   1.7、存储过程与触发器的区别
        *   1.8、悲观锁和乐观锁是什么？
        *   1.9、你常用的mysql引擎有哪些?各引擎间有什么区别? 
    *   2、Redis
        *   2.1、Redis宕机怎么解决? 
        *   2.2、redis和mecached的区别，以及使用场景
        *   2.3、Redis集群方案该怎么做?都有哪些方案?
        *   2.4、Redis回收进程是如何工作的
    *   3、MongoDB
        *   3.1、MongoDB中对多条记录做更新操作命令是什么？
        *   3.2、MongoDB如何才会拓展到多个shard里？
*   六、测试
    *   1、编写测试计划的目的是
    *   2、对关键词触发模块进行测试
    *   3、其他常用笔试题目网址汇总
    *   4、测试人员在软件开发过程中的任务是什么
    *   5、一条软件Bug记录都包含了哪些内容？
    *   6、简述黑盒测试和白盒测试的优缺点
    *   7、请列出你所知道的软件测试种类，至少5项。
    *   8、Alpha测试与Beta测试的区别是什么？
    *   9、举例说明什么是Bug？一个bug report应包含什么关键字？
*   数据结构
    *   1.1、数组中出现次数超过一半的数字-Python版
    *   1.2、求100以内的质数
    *   1.3、无重复字符的最长子串-Python实现
    *   1.4、通过2个5/6升得水壶从池塘得到3升水
    *   1.5、什么是MD5加密，有什么特点？
    *   1.6、什么是对称加密和非对称加密
    *   1.7、冒泡排序的思想？
    *   1.8、快速排序的思想？
    *   1.9、如何判断单向链表中是否有环？
    *   1.10、你知道哪些排序算法（一般是通过问题考算法）
    *   1.11、斐波那契数列
    *   1.12、如何翻转一个单链表？
    *   1.13、青蛙跳台阶问题
    *   1.14、两数之和 Two Sum
    *   1.15、搜索旋转排序数组 Search in Rotated Sorted Array
    *   1.16、Python实现一个Stack的数据结构
    *   1.17、写一个二分查找
    *   1.18、set 用 in 时间复杂度是多少，为什么？
    *   1.19、列表中有n个正整数范围在[0，1000]，进行排序；
    *   1.20、面向对象编程中有组合和继承的方法实现新的类
*   八、人工智能
    *   1.1、找出1G的文件中高频词
    *   1.2、一个大约有一万行的文本文件统计高频词
    *   1.3、怎么在海量数据中找出重复次数最多的一个？
    *   1.4、判断数据是否在大量数据中
<!-- markdown-toc end -->

# 文件操作
## 1.1 有一个jsonline格式的文件爱file.txt 大小约为10K
```
    def get_lines():
        l = []
        with open('file.txt','rb) as f:
            for eachline in f:
                l.append(eachline)
            return l

    if __name__ == '__main__':
        for e in get_lines():
            process(e) #处理每一行数据
```
现在要处理一个大小为10G的文件，但是内存只有4G，如果在只修改get_lines 函数而其他代码保持不变的情况下，应该如何实现？需要考虑的问题都有那些？
```
    def get_lines():
        l = []
        with open('file.txt','rb') as f:
            data = f.readlines(60000)
        l.append(data)
        yield l
```
要考虑的问题有：内存只有4G无法一次性读入10G文件，需要分批读入分批读入数据要记录每次读入数据的位置。分批每次读取数据的大小，太小会在读取操作花费过多时间。
## 1.2 补充缺失的代码
```
    def print_directory_contents(sPath):
    """
    这个函数接收文件夹的名称作为输入参数
    返回该文件夹中文件的路径
    以及其包含文件夹中文件的路径
    """
    import os
    for sChild in os.listdir(sPath):
        sChildPath = os.path.join(sPath,sChild)
        if os.path.isdir(sChildPath):
            print_directory_contents(sChildPath)
        else:
            print(sChildPath)
```
# 模块与包
## 2.1 输入日期， 判断这一天是这一年的第几天？
```
    import datetime
    def dayofyear():
        year = input("请输入年份: ")
        month = input("请输入月份: ")
        day = input("请输入天: ")
        date1 = datetime.data(year=int(year),month=int(month),day=int(day))
        date2 = datatime.date(year=int(year),month=1,day=1)
        return (date2-date1 +1).days
```
## 2.2 打乱一个排好序的list对象alist？
```
    import random
    alist = [1,2,3,4,5]
    random.shuffle(alist)
    print(alist)
```
# 数据类型
## 3.1 现有字典 d= {'a':24,'g':52,'i':12,'k':33}请按value值进行排序?
```
    sorted(d.items(),key=lambda x:x[1])
```
## 3.2 字典推导式
```
 d = {key:value for (key,value) in iterable}
```
## 3.3 请反转字符串 "aStr"?
```
    print("aStr"[::-1])
```
## 3.4 将字符串 "k:1 |k1:2|k2:3|k3:4"，处理成字典 {k:1,k1:2,...}
```
    str1 = "k:1|k1:2|k2:3|k3:4"
    def str2dict(str1):
        dict1 = {}
        for iterms in str1.split('|'):
            key,value = iterms.split(':'):
                dict1[key] = value
        return dict1
```
## 3.5 请按alist中元素的age由小到大排序
```
    alist = [{'name':'a','age':20},{'name':'b','age':30},{'name':'c','age':25}]
    def sort_by_age(list1):
        return sorted(alist,key=lambda x:x['age'],reverse=True)
```
## 3.6 下面代码的输出结果将是什么？
```
    list = ['a','b','c','d','e']
    print(list[10:])
```
代码将输出[],不会产生IndexError错误，就像所期望的那样，尝试用超出成员的个数的index来获取某个列表的成员。例如，尝试获取list[10]和之后的成员，会导致IndexError。然而，尝试获取列表的切片，开始的index超过了成员个数不会产生IndexError，而是仅仅返回一个空列表。这成为特别让人恶心的疑难杂症，因为运行的时候没有错误产生，导致Bug很难被追踪到。
## 3.7 写一个列表生成式，产生一个公差为11的等差数列
```
    print([x*11 for x in range(10)])
```
## 3.8 给定两个列表，怎么找出他们相同的元素和不同的元素？
```
    list1 = [1,2,3]
    list2 = [3,4,5]
    set1 = set(list1)
    set2 = set(list2)
    print(set1 & set2)
    print(set1 ^ set2)
```
## 3.9 请写出一段python代码实现删除list里面的重复元素？
```
    l1 = ['b','c','d','c','a','a']
    l2 = list(set(l1))
    print(l2)
```
用list类的sort方法:
```
    l1 = ['b','c','d','c','a','a']
    l2 = list(set(l1))
    l2.sort(key=l1.index)
    print(l2)
```
也可以这样写:
```
    l1 = ['b','c','d','c','a','a']
    l2 = sorted(set(l1),key=l1.index)
    print(l2)
```
也可以用遍历：
```
    l1 = ['b','c','d','c','a','a']
    l2 = []
    for i in l1:
        if not i in l2:
            l2.append(i)
    print(l2)
```
## 3.10 给定两个list A，B ,请用找出A，B中相同与不同的元素
```
    A,B 中相同元素： print(set(A)&set(B))
    A,B 中不同元素:  print(set(A)^set(B))
```
# 企业面试题
## 4.1 python新式类和经典类的区别？
a. 在python里凡是继承了object的类，都是新式类
b. Python3里只有新式类
c. Python2里面继承object的是新式类，没有写父类的是经典类
d. 经典类目前在Python里基本没有应用

## 4.2 python中内置的数据结构有几种？
a. 整型 int、 长整型 long、浮点型 float、 复数 complex
b. 字符串 str、 列表list、 元祖tuple
c. 字典 dict 、 集合 set

## 4.3 python如何实现单例模式?请写出两种实现方式?
第一种方法:使用装饰器
```
    def singleton(cls):
        instances = {}
        def wrapper(*args, **kwargs):
            if cls not in instances:
                instances[cls] = cls(*args, **kwargs)
            return instances[cls]
        return wrapper
    @singleton
    class Foo(object):
        pass
    foo1 = Foo()
    foo2 = Foo()
    print foo1 is foo2 #True
```
第二种方法：使用基类
New 是真正创建实例对象的方法，所以重写基类的new 方法，以此保证创建对象的时候只生成一个实例
```
    class Singleton(object):
        def __new__(cls,*args,**kwargs):
            if not hasattr(cls,'_instance'):
                cls._instance = super(Singleton,cls).__new__(cls,*args,**kwargs)
            return cls._instance
        
    class Foo(Singleton):
        pass
    
    foo1 = Foo()
    foo2 = Foo()

    print foo1 is foo2 #True
```
第三种方法：元类，元类是用于创建类对象的类，类对象创建实例对象时一定要调用call方法，因此在调用call时候保证始终只创建一个实例即可，type是python的元类
```
    class Singleton(type):
        def __call__(cls,*args,**kwargs):
            if not hasattr(cls,'_instance'):
                cls._instance = super(Singleton,cls).__call__(*args,**kwargs)
            return cls._instance
```
```
    class Foo(object):
        __metaclass__ = Singleton
    
    foo1 = Foo()
    foo2 = Foo()
    print foo1 is foo2 #True

```
## 4.4 反转一个整数，例如-123 --> -321 
```
    class Solution(object):
        def reverse(self,x):
            if -10<x<10:
                return x
            str_x = str(x)
            if str_x[0] !="-":
                str_x = str_x[::-1]
                x = int(str_x)
            else:
                str_x = str_x[1:][::-1]
                x = int(str_x)
                x = -x
            return x if -2147483648<x<2147483647 else 0
    if __name__ == '__main__':
        s = Solution()
        reverse_int = s.reverse(-120)
        print(reverse_int)
```
## 4.5 设计实现遍历目录与子目录，抓取.pyc文件
第一种方法：
```
    import os

    def getFiles(dir,suffix):
        res = []
        for root,dirs,files in os.walk(dir):
            for filename in files:
                name,suf = os.path.splitext(filename)
                if suf == suffix:
                    res.append(os.path.join(root,filename))

        print(res)
    
    getFiles("./",'.pyc')
```
第二种方法：
```
    import os
    
    def pick(obj):
        try:
            if obj.[-4:] == ".pyc":
                print(obj)
            except:
                return None
        
    def scan_path(ph):
        file_list = os.listdir(ph)
        for obj in file_list:
            if os.path.isfile(obj):
        pick(obj)
            elif os.path.isdir(obj):
                scan_path(obj)
        
    if __name__=='__main__':
        path = input('输入目录')
        scan_path(path)
```
## 4.6 一行代码实现1-100之和
```
    count = sum(range(0,101))
    print(count)
```




    
        
