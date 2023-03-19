
# CMD can be over-ride 

FROM alpine
CMD ["echo", "hello", "shaik"]

# Now let us over ride the above cmd

* docker container run shaik ls  ==> here ls is over-rided the cmd and printed the below one

bin
dev
etc
home
lib
media
mnt
opt
proc
root
run
sbin
srv
sys
tmp
usr
var

 ENTRY POINT 
 -------------

 # Let us use ENTRY POINT :- Entry point cannot be over-ride.

 FROM alpine
 ENTRYPOINT ["echo"]
CMD ["shaik"]

* `docker container run shaik ls` ==> This will only print 'ls'..

* Because the entry point cannot be over-ride so it is over riding the CMD ["shaik] as ["ls"]

*** Always remember that ENTRYPOINT cannot be over-ride only CMD can be over-ride ***