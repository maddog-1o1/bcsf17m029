
temp=input().split(' ')

M, N, T = map(int, temp)

input()



stateDesc = []

for i in range(M):
    temp=input()
    stateDesc.append(temp)

input()


rules = []
for i in range(N):
    temp=input()
    rules.append(temp)

input()


matrix = []
for i in range(M):
    temp=input().split(' ')
    temp2=list(map(int, temp))
    matrix.append(temp2)

input()


test_cases = []
for i in range(T):
    temp = input().split("\t")

    test_cases.append({
        'initial': stateDesc.index(temp[0]),
        'final': stateDesc.index(temp[1])
        })


def print_result(states):
    actions = []

    for i in range(len(states)-1):
           actions.append(
           rules[matrix[states[i]].index(states[i+1])]
       )
    print("->".join(actions))



for test_case in test_cases:
    visited = []
    frontier = []
    answer = []
    frontier.append((test_case['initial'],))


    while (len(frontier) != 0):
        state = frontier.pop(0)
        visited.append(state[-1])

        if (state[-1] == test_case['final']):
            print_result(state)
            break
        else:
            for next_state in matrix[state[-1]]:
                if next_state not in visited:
                    frontier.append(state + (next_state,))
