Category	Commands	Sample	Details	Notes
Navigation	ls	ls -la	List directory contents with details and hidden files	
Navigation	pwd	pwd	Print current working directory absolute path	
Navigation	cd	cd /var/log	Change current directory	
Navigation	locate	locate passwd	Fast filename lookup using a maintained database	
File management	mkdir	mkdir newdir	Create a new directory	
File management	rmdir	rmdir olddir	Remove an empty directory	
File management	cp	cp file.txt /tmp/	Copy files or directories (-r for recursive)	
File management	mv	mv oldname newname	Move or rename files and directories	
File management	rm	rm file.txt	Remove files or directories (use caution with -rf)	
File management	touch	touch newfile.txt	Create an empty file or update a file timestamp	
File management	ln	ln -s /path/to/target linkname	Create hard or symbolic links	
File inspection	file	file /bin/ls	Determine a file's type	
Viewing & editing	cat	cat /etc/hosts	Print small file contents to stdout	
Viewing & editing	less	less /var/log/syslog	Page through large files; supports search and navigation	
Viewing & editing	head	head -n 20 logfile	Show the first lines of a file	
Viewing & editing	tail	tail -f /var/log/syslog	Show the last lines and follow updates	
Viewing & editing	nano	nano notes.txt	Simple terminal text editor (Ctrl+O save, Ctrl+X exit)	
Viewing & editing	vi	vi notes.txt	Modal terminal editor available on most systems	
Viewing & editing	jed	jed file.txt	Alternative terminal text editor	
Search & text processing	grep	grep -R "error" /var/log	Search text patterns in files recursively	
Search & text processing	sed	sed -n '1,5p' file	Stream editor for search/replace and transforms	
Search & text processing	awk	awk '{print $1}' file	Field-oriented text processing and reporting	
Search & text processing	cut	cut -d: -f1 /etc/passwd	Extract columns or fields from text	
Search & text processing	sort	sort file.txt	Sort lines of text	
Search & text processing	uniq	`sort file.txt  \	uniq -c`	Remove duplicate adjacent lines (often used with sort)
Search & text processing	diff	diff a.txt b.txt	Show differences between two files	
Search & text processing	tee	`echo hi \	tee out.txt`	Write output to file and stdout simultaneously
Shell utilities	echo	echo "hello"	Print text to stdout	
Shell utilities	alias	alias ll='ls -la'	Create a shortcut for a command	
Shell utilities	unalias	unalias ll	Remove a previously defined alias	
Shell utilities	history	`history \	grep apt`	Show command history
Shell utilities	man	man ls	Show manual pages for a command	
Shell utilities	cal	cal 2025	Display a calendar	
Permissions & users	chmod	chmod 640 secret.txt	Change file permissions	
Permissions & users	chown	chown user:group file	Change file owner and group	
Permissions & users	sudo	sudo systemctl restart nginx	Run a command with elevated privileges	
Permissions & users	su	su -	Switch user account (to root if omitted)	
Permissions & users	whoami	whoami	Show current effective username	
Permissions & users	useradd	sudo useradd alice	Create a new user account	
Permissions & users	userdel	sudo userdel alice	Remove a user account	
Permissions & users	passwd	passwd alice	Set or change a user's password	
Compression & archiving	tar	tar czvf backup.tgz /etc	Create or extract tar archives (gzip compression shown)	
Compression & archiving	zip	zip -r a.zip folder/	Create ZIP archives	
Compression & archiving	unzip	unzip a.zip	Extract ZIP archives	
Disk & storage	df	df -h	Show filesystem disk space usage	
Disk & storage	du	du -sh /var/log	Show directory disk usage	
Process & system	ps	ps aux	Snapshot of running processes	
Process & system	top	top	Interactive process and resource viewer	
Process & system	htop	htop	Enhanced interactive process viewer (if installed)	
Process & system	uname	uname -a	Show kernel and OS details	
Process & system	time	time ls	Measure command execution time	
Process & system	systemctl	systemctl status nginx	Control and inspect systemd services	
Process & system	jobs	jobs -l	List background and suspended shell jobs	
Process & system	kill	kill 1234	Send a signal to a process (terminate by default)	
Power & maintenance	shutdown	sudo shutdown -h now	Halt or reboot the system	
Networking & DNS	ip	ip addr show	Show or configure network interfaces and addresses	
Networking & DNS	ping	ping -c 4 8.8.8.8	Test basic network connectivity	
Networking & DNS	ss	ss -tunap	Show sockets and network connections	
Networking & DNS	netstat	netstat -tuln	Show network connections and listening ports	
Networking & DNS	traceroute	traceroute 8.8.8.8	Trace the route packets take to a host	
Networking & DNS	nslookup	nslookup example.com	Query DNS for records	
Networking & DNS	dig	dig +short example.com	Flexible DNS lookup utility	
Networking tools	wget	wget https://example.com/file	Download files from the web	
Networking tools	curl	curl -I https://example.com	Transfer data with URLs; HTTP requests	
File transfer & sync	scp	scp file user@host:/path	Copy files over SSH	
File transfer & sync	rsync	rsync -avz src/ dest/	Efficient remote/local file synchronization	
Package management	apt	sudo apt update	Debian-family package management (example)	
Package management	dnf	sudo dnf install pkg	RedHat-family package management (example)	
Monitoring & troubleshooting	watch	watch -n 2 df -h	Run a command repeatedly and show output	
Monitoring & troubleshooting	hostnamectl	hostnamectl	Show or set the system hostname	
