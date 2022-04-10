# ramy-
contract Campaignyourcontent {
    uint256 favoriteNumber;

    struct People{
        uint256 favoriteNumber;
        string name;
        string description;
        string dateCreated;
        address harmonyAddress;
        
    }
    // Function to store multiple people
    People[] public people;
    mapping(string => uint256) public nameToFavoriteNumber;

     function store (uint256 _favoriteNumber) public {
        favoriteNumber = _favoriteNumber;
    }

    function retrieve() public view returns(uint256) {
        return favoriteNumber;
    }
    
// Adding the function to store multiple people to memory
// Data will only store during the execution of the function

function addPerson(string memory _name, uint256 _favoriteNumber, string memory _description,
string memory _dateCreated, address _harmonyAddress) public {
 people.push(People(_favoriteNumber, _name, _description, _dateCreated, _harmonyAddress));
 nameToFavoriteNumber[_name] = _favoriteNumber;
}

    }
