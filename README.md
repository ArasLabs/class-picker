# Class Picker

Many organizations have a class tree defined on an ItemType that includes custom forms for the classes. In this case, users are generally trained to add the new item and then select the Classification / Type control on the form first so that they can be presented with the correct class specific form before they start filling in metadata. This approach doesn't feel natural. Users should be prompted immediately with the class picker when they decide to add a new item. This is exactly what the Razorleaf Class Picker solution does.

## History

Release notes/descriptions for the original project posted on the previous Aras Projects page.

Release | Notes
--------|--------
[v3.0.0](https://github.com/ArasLabs/class-picker/releases/tag/v3.0.0) | Includes AML package for 11.0 SP7+ (Method updated for new UI)
[v2.0](https://github.com/ArasLabs/class-picker/releases/tag/v2.0) | Includes AML package and informational PDF for 11.0 SP5
[v1.0](https://github.com/ArasLabs/class-picker/releases/tag/v1.0) | Includes AML package and informational PDF.

#### Supported Aras Versions

Project | Aras
--------|------
[v3.0.0](https://github.com/ArasLabs/class-picker/releases/tag/v3.0.0) | Aras 11.0 SP7+. (Tested on 11.0 SP15)
[v2.0](https://github.com/ArasLabs/class-picker/releases/tag/v2.0) | Aras 11.0 SP5
[v1.0](https://github.com/ArasLabs/class-picker/releases/tag/v1.0) | Aras 9.x

> ###### *Please note: Aras Community Projects are provided on an "as-is" basis.*

>*Due to the wide array of possible business requirements, customizations, and use cases, we cannot guarantee compatibility or support for any given project.*

>*If you experience issues with this or any other Aras Community Project, please contact the project author and file an issue on the project's GitHub repository. You can also check out the [Aras Developer Forums](http://community.aras.com/forums/) to see if any other community members have experienced the same issue.*

## Installation

#### Important!
**Always back up your code tree and database before applying an import package or code tree patch!**

### Pre-requisites

1. Aras Innovator installed (version 11.0 SP7+ preferred)
2. Aras Package Import tool
3. Class Picker import package

### Install Steps

1. Backup your database and store the BAK file in a safe place.
2. Open up the Aras Package Import tool.
3. Enter your login credentials and click **Login**
  * _Note: You must login as root for the package import to succeed!_
4. Enter the package name in the TargetRelease field.
  * Optional: Enter a description in the Description field.
5. Enter the path to your local `..\class-picker\Import\imports.mf` file in the Manifest File field.
6. Select **Razorleaf Class Picker** in the Available for Import field.
7. Select Type = **Merge** and Mode = **Thorough Mode**.
8. Click **Import** in the top left corner.
9. Close the Aras Package Import tool.

You are now ready to login to Aras and try out the package.

## Usage

1. Log in to Aras as admin.
2. Navigate to an ItemType with Classification (i.e. Part) and attach the Method **RL - Select Class On New** as a Client Event with the event set as OnAfterNew.
3. Navigate to the Form for the ItemType chosen above and attach the Method **RL - Class Picker Form to Front** as a Form level OnLoad event.
4. Attempt to add a New Item of the above Type. The Class Picker will open on top of the add form. Select a classification. It will appear selected on the form.
5. Continue setting up a New item as ususal, including **Save/Unlock/Close** the item.

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request

For more information on contributing to this project, another Aras Labs project, or any Aras Community project, shoot us an email at araslabs@aras.com.


## Credits

**Project Owner:** Razorleaf

**Original Idea:** Dennis Lindinger

**Created On:** May 30, 2013

**Contributing** Sam Poe, Aras Labs

**Updated On:** May 17, 2019

## License

This project is published under the Microsoft Public License license (MS-PL). See the [LICENSE file](./LICENSE.md) for license rights and limitations.
