Randomization
=============

Script to create stranger to stranger pairs:::

from random import randint

strangersList = range(1,867)
nStrangers = len(strangersList) # elements in strangersList

strangerPairs = []; # start out as empty list

while (len(strangerPairs) < 280):
	# get two random strangers
	# randint(a, b) returns integer between a and b
	Rstranger1 = strangersList[randint(0, nStrangers-1)]
	Rstranger2 = strangersList[randint(0, nStrangers-1)]
	
	# if Rstranger2 == Rstranger1, keep trying a random stranger
	# (you don't want the same person to get paired with themself!)
	while (Rstranger2 == Rstranger1):
		Rstranger2 = strangersList[randint(0, nStrangers)]

	# add the tuple (Rstranger1, Rstranger2) only if it's new
	if (Rstranger1, Rstranger2) not in strangerPairs:
		strangerPairs.append( (Rstranger1, Rstranger2) )

print('Generated 280 stranger-to-stranger pairs...')
for pair in strangerPairs:
	print(pair)

SO1Pairs = []; # another empty list

while (len(SO1Pairs) < 20):
        # get one random stranger
        # randint(a, b) returns another integer within range a and b
        S1stranger = strangersList[randint(0, nStrangers-1)]

        # add the tuple (SO1, S1stranger) only if it's new
        if ('SO1', S1stranger) not in SO1Pairs:
                SO1Pairs.append( ('SO1', S1stranger) )

print('Generated 20 pairs with SO1...')
for pair in SO1Pairs:
        print(pair)

SO2Pairs = []; # another empty list

while (len(SO2Pairs) < 20):
        # get one random stranger
        # randint(a, b) returns another integer within range a and b
        S2stranger = strangersList[randint(0, nStrangers-1)]

        # add the tuple (SO2, S2stranger) only if it's new
        if ('SO2', S2stranger) not in SO2Pairs:
                SO2Pairs.append( ('SO2', S2stranger) )

print('Generated 20 pairs with SO2...')
for pair in SO2Pairs:
        print(pair)

SO3Pairs = []; # another empty list

while (len(SO3Pairs) < 20):
        # get one random stranger
        # randint(a, b) returns another integer within range a and b
        S3stranger = strangersList[randint(0, nStrangers-1)]

        # add the tuple (SO3, S3stranger) only if it's new
        if ('SO3', S3stranger) not in SO3Pairs:
                SO3Pairs.append( ('SO3', S3stranger) )

print('Generated 20 pairs with SO3...')
for pair in SO3Pairs:
        print(pair)

SO4Pairs = []; # another empty list

while (len(SO4Pairs) < 20):
        # get one random stranger
        # randint(a, b) returns another integer within range a and b
        S4stranger = strangersList[randint(0, nStrangers-1)]

        # add the tuple (SO4, S4stranger) only if it's new
        if ('SO4', S4stranger) not in SO4Pairs:
                SO4Pairs.append( ('SO4', S4stranger) )

print('Generated 20 pairs with SO4...')
for pair in SO4Pairs:
        print(pair)

print('ALL PAIRS GENERATED, MAKE MORPHS!')
