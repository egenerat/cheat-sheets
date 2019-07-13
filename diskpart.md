### Re-create partition and format
```
diskpart
list disk
select disk 0
list partition
clean
create partition primary
format fs=ntfs quick
active
assign
exit
```
