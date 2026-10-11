# Input Limitations

The race accepts the text returned by the turtle-screen input dialog without validating it against the six configured turtle colors. An empty or cancelled dialog produces a falsy value and prevents the race loop from starting. Non-empty text is retained as the user's selected value and is compared with the winning turtle color after normalization to lowercase.
