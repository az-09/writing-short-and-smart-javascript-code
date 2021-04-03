Examples from https://levelup.gitconnected.com/9-tricks-for-writing-short-and-smart-javascript-code-6c832290e0b1

# Multiple conditions

#### longhand

    if( x === 'test1' || x === 'test2' || x === 'test3'){
    }

#### shorthand

    if(['test1', 'test2', 'test3'].includes(x)){
    }

# Loops

#### longhand

    for (var i = 0; i < testList.length; i++>){
    }

#### shorthand in for index, of for element

    for (let i in testList){
    }

    for (let i of testList){
    }

    testList.forEach(e => {
    })

# Implicit return

#### longhand

    function testFunction(){
        return x \* y
    }

#### shorthand

    testFunction = z = x \* y

# Spread Operator

    const testList = ['a', 'b', 'c']

#### longhand

    const testList2 = ['x', 'y', 'z'].concat(testList)

    const newTestList = testList.slice()

#### shorthand

    const testList2 = ['x', 'y', 'z', ...testList]

    const newTestList = [...testList]

# Array.find

#### longhand

    const cars = [
        {name: 'sonata', carType: 'sedan'},
        {name: 'tusan', carType: 'SUV'},
        {name: 'santafe', carType: 'SUV'}
    ]

    function findSedan(name){
        for (let i=0; i < cars.length; ++i){
            if(cars[i].carType === 'sedan' && cars[i].name === name){
                return cars[i]
            }
        }
    }

#### shorthand

    findSedan = name => {
        cars.find(car => car.carType === 'sedan' && car.name === name)
    }
