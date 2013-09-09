Randomization
=============

Script to create stranger to stranger pairs:::


from random import randint

strangersList = range(1,869)
nStrangers = len(strangersList) # elements in strangersList

strangerPairs = []; # start out as empty list

while (len(strangerPairs) < 280):
	# get two random strangers
	# randint(a, b) returns integer between a and b
	stranger1 = strangersList[randint(0, nStrangers-1)]
	stranger2 = strangersList[randint(0, nStrangers-1)]
	
	# if stranger2 == stranger1, keep trying a random stranger
	# (you don't want the same person to get paired with themself!)
	while (stranger2 == stranger1):
		stranger2 = strangersList[randint(0, nStrangers)]

	# add the tuple (stranger1, stranger2) only if it's new
	if (stranger1, stranger2) not in strangerPairs:
		strangerPairs.append( (stranger1, stranger2) )

print('Generated 280 stranger pairs...')
for pair in strangerPairs:
	print(pair)
