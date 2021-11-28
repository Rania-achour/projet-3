Project 3 DAAR  By:

Rania ACHOUR/
Neila KHEZNADJI/
Rayan ALIM/
///////////////////////////////////////////////////////////







ON Terminal to creat user accounts and add balance:
PS C:\Users\HP\build-collective> truffle console --network development 
truffle(development)> web3.eth.personal.newAccount('test');
truffle(development)> web3.eth.personal.newAccount('Rania');
truffle(development)> web3.eth.personal.newAccount('Neila');
truffle(development)> web3.eth.personal.newAccount('Rayan');
truffle(development)> web3.eth.getAccounts().then(function(result) { accounts = result});
undefined
truffle(development)> accounts
[
  '0x4973A1540842ed9ac815B7eFf8A7039E4cfd70E3',
  '0x4B7Bbe83EAB797406695D26b5a4e254840d458E9',
  '0x7157e2639Fd7F40772b39ee0Cd048c5B7C81Ea1A',
  '0xFE84Ec25245643cC8a4Aa85f11127D73cE719cD8',
  '0x7E807f9bbA9E6E6ea06Df025E7f8e22d48097B14',
  '0xb2546a4cdC56A025E5F62720a45280b6e04cafD1',
  '0x0a8618fB76a3042406BCf9fbC23A049E262e4cc7',
  '0xc1B2d926bcd1Ef084f9eC20F429526a0c0414361',
  '0xAec796b6fB471413E3614725c86242C94DfFfEBf',
  '0x10c6E800553cd7119e5d7374EDfaF137d108811f',
  '0x380B1f992d50f993FFFB3384d7f16ba0eca4CB13',
  '0xEaC570fef551700c06899a030Dc204Ee3c9dB214',
  '0xD1F75c4B90964Cb722DeD3035e2b091C62A334d9',
  '0x9dB035503b382C3c7E47aD328eC639225Ec26ec2'
]


truffle(development)> web3.eth.sendTransaction({to:accounts[10], from:accounts[1], value:web3.utils.toWei("5", "ether")});
truffle(development)> web3.eth.sendTransaction({to:accounts[11], from:accounts[1], value:web3.utils.toWei("6", "ether")});
truffle(development)> web3.eth.sendTransaction({to:accounts[11], from:accounts[1], value:web3.utils.toWei("4", "ether")});
truffle(development)> web3.eth.sendTransaction({to:accounts[13], from:accounts[1], value:web3.utils.toWei("3", "ether")});


truffle(development)> web3.eth.getBalance(accounts[10], (err, bal) => { console.log("newAccounts", bal); } );
newAccounts 6000000000000000000
'6000000000000000000'
truffle(development)> web3.eth.getBalance(accounts[11], (err, bal) => { console.log("newAccounts", bal); } );
newAccounts 5000000000000000000
'5000000000000000000'
truffle(development)> web3.eth.getBalance(accounts[12], (err, bal) => { console.log("newAccounts", bal); } );
newAccounts 4000000000000000000
'4000000000000000000'
truffle(development)> web3.eth.getBalance(accounts[13], (err, bal) => { console.log("newAccounts", bal); } );
newAccounts 3000000000000000000
'3000000000000000000'


the rest of the code for the creation on the company you will find it in BuildCollection.sol
on a aussi creer le front avec html et css des page web pour le login des user et de l'entreprise
