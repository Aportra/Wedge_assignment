## Feedback 

Very nice README doc in this. 

It doesn't look like the submission.md document is filled in. Having this complete is contingent on getting that turned in. 

I'm glad you enjoyed the project so much! Consider finding a job in Data Engineering. If you liked this and got that deep sense of satisfaction when the pieces fit together, then you're likely to enjoy a career in DE. There are lots of gigs and they pay well. 

Nice work on this project, you can consider it complete (contingent on the table). I'm going to read your files in order and give you feedback
as I move through them, from Task 1 to Task 3. 


### Task 1

* Check out environment variables and the virtual environment world in Python. That's the way to avoid code like this: 

```
try:
    directory_small = '/Users/aaronportra/Documents/ADA/wedge_project/WedgeZipOfZips_small/'
    directory = '/Users/aaronportra/Documents/ADA/wedge_project/WedgeZipOfZips/'
    os.listdir(directory)
except FileNotFoundError:
    directory_small = 'C:\\Users\\aport\\OneDrive\\Documents\\School\\Fall Semester 2024\\Applied Data Analytics\\wedge_project\\WedgeZipOfZips_small\\'
    directory = 'C:\\Users\\aport\\OneDrive\\Documents\\School\\Fall Semester 2024\\Applied Data Analytics\\wedge_project\\WedgeZipOfZips\\'
    os.listdir(directory)
```
You can basically have your code be aware of the machine it's operating on. 

I'm surprised by these lines: 

```
if len(first_row) < 50:
        has_header = False
```
I would think that fewer than 50 columns would be a sign that you didn't have the correct delimiter, not that it didn't have a header. You've already used the `sniffer.has_header` to determine this. 

Your code to do the cleaning is much shorter than most, so I'll be curious to see the `submission.md` comparison. If this worked, it's a _very_ efficient implementation. 

`create_db` is a bit of a confusing function name. Something like `upload_to_gbq` seems more natural to me. 

### Task 2

Couldn't 

```
        with owner_sample as(

        select distinct card_no 
        from `{project_id}.{dataset_id}.transArchive_*`
        order by rand()
        limit {sample_size}
        )
        select * 
        from owner_sample;
```
Just be 

```
        select distinct card_no 
        from `{project_id}.{dataset_id}.transArchive_*`
        order by rand()
        limit {sample_size};
```

Maybe I'm missing something.

It'd be worth thinking through how you'd do this the reproducible way. That'd involve selecting distinct card numbers, pulling them down to python, calling `random.sample` and then building a query that could use them all. Let me know if it's not clear how you'd do that. 

Overall nice job on this. 

### Task 3

* Nice job on this, very efficient. 

