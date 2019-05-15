# pro1
<br>class Solution(object):</br>
 <br>   def dailyTemperatures(self, T):</br>
        """<br>
        :type T: List[int]</br>
        <br>  :rtype: List[int] </br>
        <br>""" </br> 
        res=[0]*len(T)</br>
        <br>  stack=[]</br>
        <br>  for i,t in enumerate(T):</br>
            <br>  while stack and T[stack[-1]]<t:</br>
                   <br>      cur=stack.pop()</br>
                    <br>     res[cur]=i-cur</br>
           <br>  stack.append(i)</br>
        return res</br>
