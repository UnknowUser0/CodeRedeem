![CodeRedeem](https://cdn.modrinth.com/data/cached_images/97c2a7b8e9c22393aeeee72574f95c4c83c6e1dd.png)

# **CodeRedeem**
CodeRedeem allows you to create random coupon codes for players to redeem specific rewards.

## **Features**
- The reward system is fully customizable, allowing you to define what command should be executed for each type of code specified in the configuration. You can set up redemption codes according to your preferences in the folder resources.
- Make sure to modify the codes, and rewards without needing to restart the server (auto-save). 

## **Usage**
- Usage to redeem for player
```
/redeem <Code>
```
- Usage for OP and consol

![command](https://cdn.modrinth.com/data/cached_images/79761e80ef1ce85e52425e09519960cf2cd5348c.png)

## **Warning**
However, keep in mind that manually editing the data.yml file is not recommended.

## **config.yml**

```
# Selec Language
language: en_US
# Economy
economy:

  use-vault: true

# Advance Setting
additional-settings:
  
  example-setting: "value"

```
To be honest, in config.yml it is only for setting the language. For other settings, it seems that there is no need to change them.

## **example_code.yml**
This file is located in the codes folder.
```
# REDEEM CODE
code: REDEEMCODE123

# Validity date in yyyyMMdd format
validity: 20241231

# Rewards configuration
rewards:
- item: WRITTEN_BOOK
  count: 1
  book: great_tale
- item: DIAMOND_SWORD
  count: 1
  enchantments:
  - type: SHARPNESS
    level: 5
  - type: UNBREAKING
    level: 3
- item: GOLDEN_APPLE
  count: 5
- money: 1000

# Optional: Define how many times the code can be redeemed
# Use -1 for unlimited
redeem_limit: 10

# dont change this
redeem_count: 1

```

## **en_US.yml**
This file is located in the language folder.
```
# Set your langue in this

already_redeemed: "You have already redeemed this code."
book_received: "You have received the book {title}."
code_expired: "This code has expired."
code_not_available: "Code not available."
empty_book: "The book {bookName} is empty."
error_creating_book: "There was an error creating the book: {bookName}."
error_parsing_date: "Error parsing the expiration date."
error_loading_code: "Codes folder does not exist or is not a directory."
error_processing_reward: "There was an error processing one or more rewards."
invalid_book_reference: "The book reference {bookName} is invalid or does not exist."
invalid_code: "The code you provided is invalid or does not exist."
invalid_date_format: "The date format in the code configuration is invalid."
invalid_enchantment: "Invalid enchantment:  {enchantmentName}. Please check the enchantment name."
invalid_item_material: "Invalid item material: {itemName}. Please check the item name."
invalid_reward_format: "The reward format is invalid."
invalid_subcommand: "Invalid subcommand. Use /cr help for a list of commands."
money_received: "You have received ${money}"
no_permission: "You do not have permission to use this command."
only_players: "This command can only be used by players."
plugin_reloaded: "The plugin has been reloaded successfully."
redeem_limit_reached: "The redeem limit for this code has been reached."
redeem_successful: "You have successfully redeemed the code!"
reloaded: "Plugin configuration and language reloaded successfully."
usage_subcommand: "Usage: /cr {subCommand}"
usage_info: "Usage: /cr info <code>"
usage_redeem: "Usage: /redeem <code>"
warning_throw_book: "This written book cannot be discarded."
message_received_reward: "You have received {count} {itemName}s."
inalid_number_format_for_length: "Invalid number format for length."
invalid_length: "Length must be between 6 and 16."
invalid_code_length: "Code must be beween 6 and 16 character"
success_create_code: "File created and modified successfully. New file: "
failed_create_code: "Failed to save the new file."
code_not_found_in_data: "Code not found in data"
code_refreshed: "The code was successfully refreshed"
failed_refresh_code: "The code failed to refresh"
op_only: "You must be an operator to use this command."
hold_written_book: "You must be holding a Written Book."
invalid_book: "The item in your hand is not a valid written book."
no_title: "The written book must have a title."
file_exists: "A file with this title already exists. Choose a different title."
save_success: "The book has been successfully saved as {fileName}."
save_error: "An error occurred while saving the book."

# translate for /cr info <code>
code_info_header: "Code INFORMATION"
status: "Status"
code: "Code"
validity_date: "Valid to"
redeem_limit: "Redeem Limit"
redeem_count: "Redeem Count"
file: "File Name"
```

