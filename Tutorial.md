### dp-of-yfy-1 ACWING902
<font face="微软雅黑"  size=72>
    We know that our purpose is to convert string X to string Y by replacing, deleting or inserting.<br>   
    Let's analyze it a little bit:<br>
    1. First, we have four choices for a character in string X,replacing, delete, insert or do nothing.<br>
    2. Second, we kown that each character in string X is corresponded to one of the above operations.<br>
    
    So let i denote the state of the X, and j denote the state of Y.
    Because string Y is unchangeable, so we only can change the X, think about the last character in the String X,
    If we try to delete it, we must let the i-1 become j(i-1 and j are all the states).Else if we try to insert it we must let
    the i to be j-1. Also for replacing, we must let i-1 to be j-1, for do nothing, there must be Xi = Yj, otherwise, X can't be
    the Y.
    
    In this way, we would easily get the transfer equation:
    f(i,j)=min(f(i-1,j)+1,f(i,j-1)+1)
    And if(Xi==Yj)f(i,j)=min(f(i,j),f(i-1,j-1))
    else f(i,j)=min(f(i,j),f(i-1,j-1)+1)



</font>
