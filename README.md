# squilt
Wrapper to confine quilt with [bubblewrap](https://github.com/containers/bubblewrap)

Previous versions used [nsjail](https://github.com/google/nsjail).

# Why?
Using quilt on untrusted spec files is not secure. For more see
[this posting by Matthias](https://www.openwall.com/lists/oss-security/2018/09/27/2).

Matthias developed the original exploit, but as described in the posting, any
command in %prep is run as the user calling quilt without any limitations. This
was (at least to us) unexpected.

# Usage
If you add an alias quilt=squilt or copy this script as 'quilt' to a directory
that is earlier in $PATH you should be able to use it like you use quilt without
noticying a difference.
