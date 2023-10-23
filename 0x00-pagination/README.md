# Pagination

The learning objectives of this project are:

- How to paginate a dataset with simple page and page_size parameters
- How to paginate a dataset with hypermedia metadata
- How to paginate in a deletion-resilient manner
 
**Requirements/Behavior:**
- Use `assert` to verify that `index` is in a valid range.
- If the user queries index 0, `page_size` 10, they will get rows indexed 0 to 9 included.
- If they request the next index (10) with `page_size` 10, but rows 3, 6 and 7 were deleted, the user should still receive rows indexed 10 to 19 included.