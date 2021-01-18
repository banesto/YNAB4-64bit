# 64-bit YNAB 4 converter shell script for macOS

YNAB 4 is a 32-bit application that will not run on macOS beginning with macOS Catalina. Catalina is the first version of macOS to exclusively support 64-bit applications. YNAB made an announcement that they will not update YNAB 4 to the 64-bit architecture.

This shell script will convert the final release of YNAB 4 for macOS (v4.3.855) from a 32-bit app to a native 64-bit app so that it will run on macOS Catalina without the need for an emulation or compatibility layer. You will still need a valid license key to use the 64-bit version of the app.

This shell script is not affiliated with YNAB in any way and YNAB has not endorsed this at all. YNAB has [offically ended support](https://web.archive.org/web/20191008235951/https://www.youneedabudget.com/ynab-4-support-will-end-october-2019/) for YNAB 4. Do not contact them with support requests of any kind with respect to this shell script or using YNAB 4 on macOS Catalina. You are on your own and you use at your own risk.

## Usage

To run the shell script, do the following:

1. Press `Command (⌘) + Space`
2. Type `Terminal` and press Enter
3. Copy and paste the following into the terminal window and press Enter (be sure to include the ending quote). The script explains what it will do and then pauses before it does it.

   ```/bin/sh -c "$(curl -fsSL https://gitlab.com/bradleymiller/Y64/raw/master/install)"```

4. When the shell script is complete, you must drag the resulting app to your /Applications directory to install

## How It Works

YNAB 4 is not written in a compiled language. It is written in ActionScript and interpreted by the Adobe AIR runtime when you run the program. As a result, it is the Adobe AIR runtime that needs to be updated to the 64-bit architecture, not the ActionScript. The final release of YNAB 4 is packaged with the 32-bit AIR runtime and this shell script replaces it with the 64-bit runtime provided by Adobe. The resulting app is a native 64-bit app that runs without an emulation/compatibility layer.

## Limitations
- Will not work with App Store purchased licenses unless you have received a separate license key. Refer to YNAB's [Mac App Store FAQ](https://web.archive.org/web/20170817002804/https://classic.youneedabudget.com/support/article/mac-app-store-faq).
- The `Check for Updates` function does not work.

## Other Methods

You may be able to run macOS Mojave or Windows in a virtual machine to run the 32-bit app on Catalina.

## Legal Stuff
**IMPORTANT NOTE:** This shell script is not affiliated with YNAB in any way and YNAB has not endorsed this at all. You Need a Budget and YNAB are registered trademarks of You Need A Budget LLC and/or one of its subsidiaries.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
