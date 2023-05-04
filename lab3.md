# Lab Report 3
## Command we are going to focus `Find`!
Here is the path to technical folder: `/Users/Wally/Desktop/CSE15L/docsearch/technical`

## `-maxdepth levels`
The -maxdepth option is used with the find command in Linux to specify the maximum depth of the directory hierarchy to search. It limits the search to a certain level of directories, starting from the starting directory.(Description from ChatGPT)
Input:
`find /Users/Wally/Desktop/CSE15L/docsearch/technical -maxdepth 1 -name "#.txt"`
Output:

Input:
`find /Users/Wally/Desktop/CSE15L/docsearch/technical -maxdepth 2 -name "#.txt"`
Output:
`
/Users/Wally/Desktop/CSE15L/docsearch/technical/plos/pmed.0020273.txt
/Users/Wally/Desktop/CSE15L/docsearch/technical/plos/journal.pbio.0030032.txt
/Users/Wally/Desktop/CSE15L/docsearch/technical/plos/pmed.0020065.txt
...
/Users/Wally/Desktop/CSE15L/docsearch/technical/911report/chapter-12.txt
/Users/Wally/Desktop/CSE15L/docsearch/technical/911report/chapter-10.txt
/Users/Wally/Desktop/CSE15L/docsearch/technical/911report/chapter-11.txt
`

In the first example, because there is no txt file in the current directory( maxdepth 1), so nothing return. 
In the second example, there are tons of txt file when the depth = 2, so it returns a lot of txt file. 

## `-mindepth levels`
The -mindepth option is used with the find command in Linux to specify the minimum depth of the directory hierarchy to search. It allows you to limit the search to directories that are at a certain level or deeper, starting from the starting directory.(Description from ChatGPT)

Input:
`find /Users/Wally/Desktop/CSE15L/docsearch/technical -mindepth 2 -name "#.txt"`
Output:
`
/Users/Wally/Desktop/CSE15L/docsearch/technical/plos/pmed.0020273.txt
/Users/Wally/Desktop/CSE15L/docsearch/technical/plos/journal.pbio.0030032.txt
/Users/Wally/Desktop/CSE15L/docsearch/technical/plos/pmed.0020065.txt
...
/Users/Wally/Desktop/CSE15L/docsearch/technical/911report/chapter-12.txt
/Users/Wally/Desktop/CSE15L/docsearch/technical/911report/chapter-10.txt
/Users/Wally/Desktop/CSE15L/docsearch/technical/911report/chapter-11.txt
`

Input:
`find /Users/Wally/Desktop/CSE15L/docsearch/technical -mindepth 4 -name "#.txt"`
Output:


In the first example, there are tons of txt file when the depth = 2 and depth = 3, so it returns a lot of txt file. 
In the second example, there are no txt file in the depth >= 4, so nothing returns


## `-empty`
The -empty option is used with the find command in Linux to search for empty files or directories. It returns a list of all files or directories that are empty. (Description from ChatGPT)

Input:
`find /Users/Wally/Desktop/CSE15L/docsearch/technical -type f -empty`
Output:

Input:
`find /Users/Wally/Desktop/CSE15L/docsearch/technical -type d -empty`
Output:

In the first example, we are looking for if there are empty file(`-type f`) in technical folder, and it return nothing indicating there are no empty file. All of the file contain something
In the second example, we are looking for if there are empty directory, such as empty folder, and it return nothing indicating there are no empty file. All of the folder contain some files. 

## `-mmin n`
The -mmin n option is used with the find command in Linux to search for files and directories that were modified n minutes ago. It allows you to search for files based on their modification time. (Description from ChatGPT)

Input:
`find /Users/Wally/Desktop/CSE15L/docsearch/technical -type d -mmin +30`
Output:
`/Users/Wally/Desktop/CSE15L/docsearch/technical
/Users/Wally/Desktop/CSE15L/docsearch/technical/government
/Users/Wally/Desktop/CSE15L/docsearch/technical/government/About_LSC
/Users/Wally/Desktop/CSE15L/docsearch/technical/government/Env_Prot_Agen
/Users/Wally/Desktop/CSE15L/docsearch/technical/government/Alcohol_Problems
/Users/Wally/Desktop/CSE15L/docsearch/technical/government/Gen_Account_Office
/Users/Wally/Desktop/CSE15L/docsearch/technical/government/Post_Rate_Comm
/Users/Wally/Desktop/CSE15L/docsearch/technical/government/Media
/Users/Wally/Desktop/CSE15L/docsearch/technical/plos
/Users/Wally/Desktop/CSE15L/docsearch/technical/biomed
/Users/Wally/Desktop/CSE15L/docsearch/technical/911report`

Input:
`find /Users/Wally/Desktop/CSE15L/docsearch/technical -type f -mmin -30`
Output:

In the first example, we are finding directory(`-type d`) that modified more 30 minutes ago. Since I did not modify any file in 30 minutes, so it return all of the folders in technical.
In the second example, we are finding the file(`-type f`) that modified less than 30 minutes ago. Since I did not modify any file in 30 minutes, so it return nothing. 
