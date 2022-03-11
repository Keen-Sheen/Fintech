# PyChain Ledger

![alt=""]('blockchain_application.png')


I have made the following updates to the provided Python file

1. I created a new data class named `Record`. This class will serve as the blueprint for the financial transaction records that the blocks of the ledger will store.

2. I have modifed the existing `Block` data class to store `Record` data.

3. I also added Relevant User Inputs to the Streamlit interface.

4. Finally I tested the PyChain Ledger by Storing Records.

### 1: Create a Record Data Class

I defined a new Python data class named `Record` and gave this new class a formalized data structure that consists of the `sender`, `receiver`, and `amount` attributes. To do this I had to do the following

1. Defined a new class named `Record`.

2. Added the `@dataclass` decorator immediately before the `Record` class definition.

3. Added an attribute named `sender` of type `str`.

4. Added an attribute named `receiver` of type `str`.

5. Added an attribute named `amount` of type `float`.

### 2: Modified the Existing Block Data Class to Store Record Data

I renamed the `data` attribute in the `Block` class to `record`, and then set it to use an instance of the new `Record` class that I created in the previous section. The Following steps were:

1. In the `Block` class, renamed the `data` attribute to `record`.

2. Set the data type of the `record` attribute to `Record`.

### Step 3: Added Relevant User Inputs to the Streamlit Interface

I have coded additional input areas for the user interface of my Streamlit application. I created these input areas to capture the sender, receiver, and amount for each transaction that will be stored in the `Block` record. These steps were:

1. Deleting the `input_data` variable from the Streamlit interface.

2. Adding an input area where I could get a value for `sender` from the user.

3. Adding an input area where I could get a value for `receiver` from the user.

4. Adding an input area where I could get a value for `amount` from the user.

5. As part of the “Add Block” button functionality, I updated `new_block` so that `Block` consists of an attribute named `record`, which is set equal to a `Record` that contains the `sender`, `receiver`, and `amount` values. The updated `Block` also includes the attributes for `creator_id` and `prev_hash`.

### Step 4: Test the PyChain Ledger by Storing Records

I tested the complete `PyChain` ledger and user interface by running your Streamlit application and storing some mined blocks in my `PyChain` ledger. I also tested the blockchain validation process by using the `PyChain` ledger. These following steps were:

1. In the terminal, navigateing to the project folder where I stored the coded.

2. In the terminal, run the Streamlit application by using `streamlit run pychain.py`.

3. Enter values for the sender, receiver, and amount, and then click the Add Block button. I did this several times to store several blocks in the ledger.

4. Verified the block contents and hashes in the Streamlit dropdown menu. Took a screenshot of the Streamlit application page, which was detailed with a blockchain that consists of multiple blocks. I have also included a screenshot in the `README.md` file.

![@](https://github.com/Keen-Sheen/fintech-homework/blob/main/Pychain%20Blockchain/PyChain_Ledger.png)
