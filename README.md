Hello
Here are cut up version of rockyou so that we can use it on multiple machines.
# Clean the file
sed -i 's/^\([^:]*\):[\*!]*/\1:/' hashlist.txt
sed -i '/::/d' hashlist.txt

# Prepare for Hashcat
cut -d: -f2 hashlist.txt > hashes_for_hashcat.txt
