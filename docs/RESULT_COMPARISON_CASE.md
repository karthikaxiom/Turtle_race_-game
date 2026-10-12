# Result Comparison Case

The final comparison lowercases the detected winner color before comparing it with the user's stored bet using `user_bet.lower()`.

This makes the result comparison insensitive to capitalization entered in the bet, while the stored input itself is not rewritten at capture time.
