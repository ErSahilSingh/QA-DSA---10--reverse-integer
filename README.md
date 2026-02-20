# QA-DSA---10--reverse-integer

/**
 * @param {number} x
 * @return {number}
 */
var reverse = function(x) {

    let duplicatex=x;
    x=Math.abs(x);
    let rev =0
    while(x>0){
        let rem = x%10
        rev = (10*rev)+rem;
        x=Math.floor(x/10);
    }
    let limit = Math.pow(2,31)
    if(rev < -limit || rev> limit){
        return 0
    }
    return duplicatex<0? -rev: rev
    
};
