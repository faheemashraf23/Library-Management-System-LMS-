
# Library Management System

This project has six tables is (`admins` ,`authors` ,`books` ,`category` ,`issued_books` ,`users`)

Which are given below:
## All the MySQL Query

#### Table structure for table `admins`

```http
  CREATE TABLE `admins` (
  `id` int(11) NOT NULL,
  `name` varchar(100) NOT NULL,
  `email` varchar(100) NOT NULL,
  `password` varchar(250) NOT NULL,
  `mobile` int(10) NOT NULL
  ) 
```
#### Dumping data for table `admins`

```http
  INSERT INTO `admins` (`id`, `name`, `email`, `password`, `mobile`) VALUES
  (1, 'Fahim', 'fahim15-4375@diu.edu.bd', '235689', 1956000049);
```

#### Table structure for table `authors`

```http
  CREATE TABLE `authors` (
  `author_id` int(11) NOT NULL,
  `author_name` varchar(250) NOT NULL
  )
```
#### Dumping data for table `authors`

```http
INSERT INTO `authors` (`author_id`, `author_name`) VALUES
(101, 'Md. Hasanuzzaman Dipu'),
(102, 'Tapasy Rabeya'),
(103, 'Abdullah Al Kafi'),
(104, 'Abdullah Al Shafi'),
(105, 'Abdus Sattar'),
(106, 'Syeda Maria Rahman'),
(107, 'Ms. Fatama Jannat Tisha');
```


#### Table structure for table `books`

```http
 CREATE TABLE `books` (
  `book_id` int(11) NOT NULL,
  `book_name` varchar(250) NOT NULL,
  `author_id` int(11) NOT NULL,
  `cat_id` int(11) NOT NULL,
  `book_no` varchar(250) NOT NULL,
  `book_price` int(11) NOT NULL
)
```
#### Dumping data for table `books`

```http
INSERT INTO `books` (`book_id`, `book_name`, `author_id`, `cat_id`, `book_no`, `book_price`) VALUES
(1, 'Web Engineering', 101, 2, 'CSE-414', 670),
(2, 'Computer Graphics', 102, 2, 'CSE-421', 470),
(3, 'Natural Language Processing', 103, 2, 'CSE-445', 470),
(4, 'Web Engineering Lab', 101, 2, 'CSE-415', 770),
(5, 'Computer Graphics Lab', 102, 2, 'CSE-422', 270),
(6, 'Information Security', 104, 2, 'CSE-423', 370),
(7, 'Software Engineering', 105, 2, 'CSE-333', 640);
```


#### Table structure for table `category`

```http
CREATE TABLE `category` (
  `cat_id` int(11) NOT NULL,
  `cat_name` varchar(100) NOT NULL
)
```
#### Dumping data for table `category`

```http
INSERT INTO `category` (`cat_id`, `cat_name`) VALUES
(1, 'Faculty of Business and Entrepreneurship (FBE)'),
(2, 'Faculty of Science and Information Technology (FSIT)'),
(3, 'Faculty of Engineering (FE)'),
(4, 'Faculty of Health and Life Sciences (FHLS)'),
(5, 'Faculty of Humanities and Social Sciences (FHSS)');
```


#### Table structure for table `issued_books`

```http
CREATE TABLE `issued_books` (
  `s_no` int(11) NOT NULL,
  `book_no` varchar(200) NOT NULL,
  `book_name` varchar(200) NOT NULL,
  `book_author` varchar(200) NOT NULL,
  `student_id` int(11) NOT NULL,
  `status` int(11) NOT NULL,
  `issue_date` longtext NOT NULL
)
```
#### Dumping data for table `issued_books`

```http
INSERT INTO `issued_books` (`s_no`, `book_no`, `book_name`, `book_author`, `student_id`, `status`, `issue_date`) VALUES
(1, 'CSE331', 'Compiler Design', 'Ms. Fatama Jannat Tisha', 4375, 1, '2025-04-22'),
(18, 'CSE332', 'Compiler Design Lab', 'Ms. Fatama Jannat Tisha', 4375, 2, '2025-04-22');
```


#### Table structure for table `users`

```http
CREATE TABLE `users` (
  `student_id` int(11) NOT NULL,
  `name` varchar(50) NOT NULL,
  `email` varchar(100) NOT NULL,
  `password` varchar(100) NOT NULL,
  `mobile` int(10) NOT NULL,
  `address` varchar(250) NOT NULL
) 
```
#### Dumping data for table `users`

```http
INSERT INTO `users` (`id`, `name`, `email`, `password`, `mobile`, `address`) VALUES
(4375, 'faheem', 'faheem23@gmail.com', '235689', 1902260748, 'Dattapara, Ashulia , Dhaka'),
(4376, 'akash', 'akash23@gmail.com', '235689', 1956000049, 'Khagan-Bazer, Ashulia , Dhaka');
```



## Add to PRIMARY KEY

#### Table structure for table `admins`

```http
ALTER TABLE `admins`
ADD PRIMARY KEY (`id`);
```
#### Table structure for table `authors`

```http
ALTER TABLE `authors`
ADD PRIMARY KEY (`author_id`);
```
#### Table structure for table `books`
```http
ALTER TABLE `books`
ADD PRIMARY KEY (`book_id`);
```
#### Table structure for table `category`

```http
ALTER TABLE `category`
ADD PRIMARY KEY (`cat_id`);
```
#### Table structure for table `issued_books`
```http
ALTER TABLE `issued_books`
ADD PRIMARY KEY (`s_no`);
```
#### Table structure for table `users`

```http
ALTER TABLE `users`
ADD PRIMARY KEY (`id`);
```
