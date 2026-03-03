# Procedural-programming
checkpoint
Algorithm SumOfDistinct(Set1, n1, Set2, n2)

Declare sum ← 0
Declare found

// Check elements of Set1
For i ← 0 to n1 - 1
    found ← false
    
    For j ← 0 to n2 - 1
        If Set1[i] = Set2[j] Then
            found ← true
            Break
        End If
    End For
    
    If found = false Then
        sum ← sum + Set1[i]
    End If
End For

// Check elements of Set2
For i ← 0 to n2 - 1
    found ← false
    
    For j ← 0 to n1 - 1
        If Set2[i] = Set1[j] Then
            found ← true
            Break
        End If
    End For
    
    If found = false Then
        sum ← sum + Set2[i]
    End If
End For

Print sum

End Algorithm




Procedure dot_product(v1, v2, n, ps)

ps ← 0

For i ← 0 to n - 1
    ps ← ps + (v1[i] * v2[i])
End For

End Procedure

Algorithm CheckOrthogonal

Input number_of_pairs

For k ← 1 to number_of_pairs

    Input n   // size of vectors
    
    Declare v1[n], v2[n]
    
    For i ← 0 to n - 1
        Input v1[i]
    End For
    
    For i ← 0 to n - 1
        Input v2[i]
    End For
    
    Declare ps
    
    Call dot_product(v1, v2, n, ps)
    
    If ps = 0 Then
        Print "Vectors are Orthogonal"
    Else
        Print "Vectors are Not Orthogonal"
    End If

End For

End Algorithm

Function dot_product(v1, v2, n)

Declare ps ← 0

For i ← 0 to n - 1
    ps ← ps + (v1[i] * v2[i])
End For

Return ps

End Function

Algorithm CheckOrthogonal_Function

Input number_of_pairs

For k ← 1 to number_of_pairs

    Input n
    
    Declare v1[n], v2[n]
    
    For i ← 0 to n - 1
        Input v1[i]
    End For
    
    For i ← 0 to n - 1
        Input v2[i]
    End For
    
    ps ← dot_product(v1, v2, n)
    
    If ps = 0 Then
        Print "Vectors are Orthogonal"
    Else
        Print "Vectors are Not Orthogonal"
    End If

End For

End Algorithm

