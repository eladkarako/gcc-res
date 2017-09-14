<pre>
windres --input "resources.rc" --output-format "coff" --output "resources.o"
</pre>

<pre>
gcc -g -Wall -std=gnu99 -O0   foo1.c  foo2.c foo2.c  -o aria2c.exe  resources.o 
</pre>

(or <code>gcc -o aria2c.exe  resources.o -lmsvcr90</code>)


<hr/>

the manifest and version-info are compiled from the rc file.


for a library (dll file) use: <code>2 RT_MANIFEST manifest.manifest</code>,
for an execute use: <code>1 RT_MANIFEST manifest.manifest</code>.

<hr/>

resources:
<a href="https://msdn.microsoft.com/en-us/library/ms235591(VS.80).aspx">https://msdn.microsoft.com/en-us/library/ms235591(VS.80).aspx</a>

