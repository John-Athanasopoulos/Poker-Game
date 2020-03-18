import random

def compare(z):
    sty4 = ["0","1","2","3","4","5","6","7","8","9","10","jack","queen","king","ace"]
    p1 = p1h[z]
    p2 = p2h[z]
    s1 = sty4.index(p1)
    s2 = sty4.index(p2)
    if s1 > s2:
        print("Player wins!")
    elif s2 > s1:
        print("Computer wins!")
    else:
        compare(z+1)


def split(list12, str12):
    if str12 == "H10" or str12 == "S10" or str12 == "C10" or str12 == "D10":
        if str12 == "H10":
            list12.append("H")
        elif str12 == "S10":
            list12.append("S")
        elif str12 == "C10":
            list12.append("C")
        elif str12 == "D10":
            list12.append("D")
        list12.append("10")
    elif str12 == "H Ace" or str12 == "S Ace" or str12 == "C Ace" or str12 == "D Ace":
        if str12 == "H Ace":
            list12.append("H")
        elif str12 == "S Ace":
            list12.append("S")
        elif str12 == "C Ace":
            list12.append("C")
        elif str12 == "D Ace":
            list12.append("D")
        list12.append("ace")
    elif str12 == "H King" or str12 == "S King" or str12 == "C King" or str12 == "D King":
        if str12 == "H King":
            list12.append("H")
        elif str12 == "S King":
            list12.append("S")
        elif str12 == "C King":
            list12.append("C")
        elif str12 == "D King":
            list12.append("D")
        list12.append("king")
    elif str12 == "H Queen" or str12 == "S Queen" or str12 == "C Queen" or str12 == "D Queen":
        if str12 == "H Queen":
            list12.append("H")
        elif str12 == "S Queen":
            list12.append("S")
        elif str12 == "C Queen":
            list12.append("C")
        elif str12 == "D Queen":
            list12.append("D")
        list12.append("queen")
    elif str12 == "H Jack" or str12 == "S Jack" or str12 == "C Jack" or str12 == "D Jack":
        if str12 == "H Jack":
            list12.append("H")
        elif str12 == "S Jack":
            list12.append("S")
        elif str12 == "C Jack":
            list12.append("C")
        elif str12 == "D Jack":
            list12.append("D")
        list12.append("jack")
    else:
        for char in str12:
            list12.append(char)
    
    
def straight_flush(li,Player,lih):
    for f in Player:
        split(li,f)
    for d in arr1:
        if li.count(d) == 5:
            sty = ["2","3","4","5","6","7","8","9","10","jack","queen","king","ace"]
            for d in range(9):
                high_n = []
                if sty[d] in li and sty[d+1] in li and sty[d+2] in li and sty[d+3] in li and sty[d+4] in li:
                    print("Player has a Straight on " + sty[d+4])
                    high_n.append(sty[d+4])
            if "ace" in li and "5" in li and "2" in li and "3" in li and "4" in li:
                high_n.append("5")
            else:
                high_n.append("0")
            print("high_n: " + str(high_n))
            lih.append(max(high_n))
            break
        else:
            if d == "D":
                lih.append("0")


def straight(li,Player,lih):
    for f in Player:
        split(li,f)
    sty = ["2","3","4","5","6","7","8","9","10","jack","queen","king","ace"]
    for d in range(9):
        high_n = []
        if sty[d] in li and sty[d+1] in li and sty[d+2] in li and sty[d+3] in li and sty[d+4] in li:
            print("Player has a Straight on " + sty[d+4])
            high_n.append(sty[d+4])
    if "ace" in li and "5" in li and "2" in li and "3" in li and "4" in li:
        high_n.append("5")
    else:
        high_n.append("0")
    lih.append(max(high_n)) 

def full_house(li,Player,lih):
    for f in Player:
        split(li,f)
    sty = ["2","3","4","5","6","7","8","9","10","jack","queen","king","ace"]
    sty2 = sty
    high_n = ["0"]
    for d in sty:
        sty2 = sty
        if li.count(d) == 3:
            sty2.remove(d)
            for x in sty2:
                if li.count(x) == 2:
                    high_n.append(d)
                    if li.count(x) == 3:
                        high_n.append(x)
                        print(high_n)
                    
                    
    for d in sty:
        if li.count(d) == 3 and confirm == "1":
            high_n.append(d)
            print(high_n)
        if len(high_n) == 2: 
            if high_n[0] < high_n[1]:
                lih.append(high_n[1])
                break
            else:
                lih.append(high_n[0])
                break
        elif len(high_n) == 1:
            lih.append(high_n[0])
            break
        else:
            if d == "ace":
                lih.append("0")
                break
            else:
                pass

def kind3(li,Player,lih):
    for f in Player:
        split(li,f)
    sty = ["2","3","4","5","6","7","8","9","10","jack","queen","king","ace"]
    for d in sty:
        if li.count(d) >= 3:
            lih.append(d)
            break
        else:
            if d == "ace":
                lih.append("0")
            else:
                pass
   
def kind4(li,Player,lih): 
    for f in Player:
        split(li,f)
    sty = ["2","3","4","5","6","7","8","9","10","jack","queen","king","ace"]
    for d in sty:
        if li.count(d) == 4:
            lih.append(d)
            break #kind4p1 and kind4p2 have 7 cards each. So there can be a Four of a kind for at most one number 
        else:
            if d == "ace":
                lih.append("0")
            else:
                pass

def flush(li,Player,lih):
    for f in Player:
        split(li,f)
    for d in arr1:
        if li.count(d) >= 5:
            indices = [i for i, x in enumerate(li) if x == d]
            flush_cards = []
            for i in indices:
                flush_cards.append(li[i+1])
            highest_card = 0
            for i in flush_cards:
                if i == "ace":
                    highest_card = "ace"
                    break
                elif i == "king" and highest_card!="ace":
                    highest_card = "king"
                    break
                elif i == "queen" and highest_card != "ace" and highest_card != "king":
                    highest_card = "queen"
                    break
                elif i == "jack" and highest_card != "ace" and highest_card != "king" and highest_card != "queen":
                    highest_card = "jack"
                    break
                elif int(i) > highest_card:
                    highest_card = i
                else:
                    pass
            lih.append(highest_card)
            break
        else:
            if d == "D":
                lih.append("0")
            else:
                pass


def high_card(li,Player,lih):
    for f in Player:
        split(li,f)
    sty = ["2","3","4","5","6","7","8","9","10","jack","queen","king","ace"]
    sty3 = sty
    sty3.reverse()
    for d in sty3:
        if d in li:
            for i in range(li.count(d)):
                lih.append(d)


def two_pair(li,Player,lih):
    for f in Player:
        split(li,f)
    sty = ["2","3","4","5","6","7","8","9","10","jack","queen","king","ace"]
    sty2 = sty
    sty3 = sty
    sty3.reverse()
    pairs = []
    for i in sty:
        if li.count(i) == 2:
            pairs.append(i)
    if len(pairs) == 0:
        lih.append("0")
        lih.append("0")
        lih.append("0")
    elif len(pairs) == 1:
        lih.append("0")
        lih.append("0")
        lih.append(pairs[0])
    else:
        for d in sty3:
            if d in pairs:
                lih.append(d)
            else:
                pass
        for d in sty3:
            if d in pairs:
                lih.append(d)
                break
            else:
                pass


arr1 = ["H","S","C","D"] #h stands for hearts, s for spades, c for clubs and d for diamonds
arr2 = ["2","3","4","5","6","7","8","9","10"," Jack"," Queen"," King"," Ace"] #all the numbers of the cards
Player = [] #Player's cards
Computer = [] #Computer's cards
p1h = [] #Player's hand
p1hn = [] #list to compare with p1h to know if Player has a type of hand or not
p2h = [] #Computer's hand
p2hn = []
cards = [] #all the cards of the deck
cards12 = [] #every time a card is asigned to either the Player or the Computer, cards12 = cards - (selected card)
for i in arr1:
    for j in arr2:
        cards.append(i+j)
print("____________________________________________________________________________________________________________________________________________________________________________")
print("Deck: ")
print(cards)
print("____________________________________________________________________________________________________________________________________________________________________________")
cards12 = cards
for a in range(5):
    scp1 = cards12[random.randrange(51-2*a)] #selects a random card for Player // after i rounds, the cards already selected are 2*i, so the remaining cards are in range of 51-2*i
    Player.append(scp1) #adds it to the Player's list
    cards12.remove(scp1) #removes it from cards12
    scp2 = cards12[random.randrange(50-2*a)]#selects a random card from the remaining cards (cards12) for Computer // same logic as before, but the Computer's remaining cards are 1 less than Player's (51-2*i-1)
    Computer.append(scp2)
    cards12.remove(scp2)
print("Player's Hand: ")
print (Player)
print("____________________________________________________________________________________________________________________________________________________________________________")
print("Computer's Hand: ")
print (Computer)
print("____________________________________________________________________________________________________________________________________________________________________________")

#Check for straight flush
str_flp1 = []
str_flp2 = []

straight_flush(str_flp1,Player,p1h)
straight_flush(str_flp2,Computer,p2h)

#Check for Four of a kind
kind4p1 = []
kind4p2 = []

kind4(kind4p1,Player,p1h)
kind4(kind4p2,Computer,p2h)

#Check for Full House
fullhp1 = []
fullhp2 = []

full_house(fullhp1,Player,p1h)
full_house(fullhp2,Computer,p2h)

#Check for flush
flushp1 = []
flushp2 = []

flush(flushp1,Player,p1h)
flush(flushp2,Computer,p2h)

#Check for straight
straightp1 = []
straightp2 = []

straight(straightp1,Player,p1h)
straight(straightp2,Computer,p2h)

#Check for Three of a kind
kind3p1 = []
kind3p2 = []

kind3(kind3p1,Player,p1h)
kind3(kind3p2,Computer,p2h)

#Check for Two Pairs
tpp1 = []
tpp2 = []
two_pair(tpp1,Player,p1h)
two_pair(tpp2,Computer,p2h)

#Check for high_card
hcp1 = []
hcp2 = []

high_card(hcp1,Player,p1h)
high_card(hcp2,Computer,p2h)

print("Player's hand: " + str(p1h))
print("Computer's hand: " + str(p2h))
print(" ")

compare(0)

#Hope you enjoy!
