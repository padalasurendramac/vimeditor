For example, to search for the first occurrence of the string ‘foo’ in the current line and replace it with ‘bar’, you would use:

`:s/foo/bar/`


Copy
To replace all occurrences of the search pattern in the current line, add the g flag:

`:s/foo/bar/g`

If you want to search and replace the pattern in the entire file, use the percentage character % as a range. This character indicates a range from the first to the last line of the file:

`:%s/foo/bar/g`

If the {string} part is omitted, it is considered as an empty string, and the matched pattern is deleted. The following command deletes all instances of the string ‘foo’ in the current line:

`:s/foo//g`

To confirm each substitution, use the c flag:

`:s/foo/bar/gc`

Copy
replace with bar (y/n/a/q/l/^E/^Y)?
Copy
Press y to replace the match or l to replace the match and quit. Press n to skip the match and q or Esc to quit substitution. The a option substitutes the match and all remaining occurrences of the match. To scroll the screen down, use CTRL+Y, and to scroll up, use CTRL+E.
