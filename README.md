# AuctionProgram.py
About the Auction selection processes of the  bid
import os
def findwinner(bidderdetails):
    highestbid=0
    winner=" "
    for bidder in bidderdetails:
        biddingprice=bidderdetails[bidder]
        if biddingprice > highestbid:
            highestbid=biddingprice
            winner=bidder
            
    print(bidderdetails)        
    print(f"The Winner is {winner} with a bid price of {highestbid}")
            
bidderdata={}
endofbidding=False
while not endofbidding:
    name=input("What is your name:")
    price=int(input("What is your bid? :"))
    bidderdata[name]=price
    morebidders=input("Are there more bidders? Type 'Yes' or 'no' :").lower()
    if morebidders=='no':
        endofbidding=True
        findwinner(bidderdata)
    elif morebidders=='Yes':
        os.system('cls')
