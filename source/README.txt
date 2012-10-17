======================
 README: Docutils 0.9
======================

:Author: David Goodger
:Contact: goodger@python.org
:Date: $Date$
:Web site: http://docutils.sourceforge.net/
:Copyright: This document has been placed in the public domain.

.. contents::


.. Quick-Start
   ===========

.. _Quick-Start:

クイックスタート
================

.. This is for those who want to get up & running quickly.

これは直ぐに始めたい & さっそく実行したい人のためのものです。

.. 1. Docutils requires Python (version 2.3 or later), available from

        http://www.python.org/

      See Requirements_ below for details.

   2. Use the latest Docutils code.  Get the code from the `Subversion
      repository`_ or from the snapshot:

        http://docutils.svn.sourceforge.net/viewvc/docutils/trunk/docutils/?view=tar

      See `Releases & Snapshots`_ below for details.

   3. Unpack the tarball in a temporary directory (**not** directly in
      Python's ``site-packages``), go to the directory created by expanding
      the archive, and run ``setup.py install`` with admin rights. On
      Windows systems it may be sufficient to double-click ``install.py``.

      See Installation_ below for details.

   4. Use the front-end scripts to convert reStructuredText documents.
      Try for example::

          rst2html.py FAQ.txt FAQ.html         (Unix)
          python tools/rst2html.py FAQ.txt FAQ.html  (Windows)

      See Usage_ below for details.

1. Docutils には

     http://www.pyhton.org/

   から入手出来る Python （バージョン 2.3 またはそれ以降）が必要です。

   詳細については下記の `必要条件`_ を参照してください。

2. 最新の Docutils コードを使ってください。 `Subversion リポジトリ`_
   またはスナップショットからコードを入手します:

     http://docutils.svn.sourceforge.net/viewvc/docutils/trunk/docutils/?view=tar

   詳細については下記の `リリース & スナップショット`_ を参照してください。

3. テンポラリのディレクトリ（直接 Python の ``site-packages`` ディレクトリに
   **入れないで** ください）に TAR ボールを解凍し、アーカイブを展開してできた
   ディレクトリに移動し、管理者の権限で ``setup.py install`` を実行します。
   ウィンドウシステムでは ``install.py`` をダブルクリックすれば十分でしょう。

   詳細については下記の インストレーション_ を参照してください。

4. reStructuredText ドキュメントを変換するにはフロントエンドスクリプトを使います。
   次の例を試してください::

       rst2html.py FAQ.txt FAQ.html         (Unix)
       python tools/rst2html.py FAQ.txt FAQ.html  (Windows)

   詳細については下記の 使い方_ を参照してください。

.. Purpose
   =======

目的
====

.. The purpose of the Docutils project is to create a set of tools for
   processing plaintext documentation into useful formats, such as HTML,
   XML, and LaTeX.  Support for the following sources has been
   implemented:

Docutils プロジェクトの目的は、プレーンテキストのドキュメントをHTML、XML、\
そして LaTeX などのような便利な書式に加工するための道具のセットを作ることです。
以下のソースのサポートが実装されています:

.. * Standalone files.

   * `PEPs (Python Enhancement Proposals)`_.

   Support for the following sources is planned:

   * Inline documentation from Python modules and packages, extracted
     with namespace context.

   * Email (RFC-822 headers, quoted excerpts, signatures, MIME parts).

   * Wikis, with global reference lookups of "wiki links".

   * Compound documents, such as multiple chapter files merged into a
     book.

   * And others as discovered.

* 単一ファイル

* `PEP (Python 拡張提案)`_

以下のソースのサポートを予定しています:

* Python モジュールやパッケージから、名前空間の文脈に沿って抽出されたインラインドキュメント

* E メール（RFC-822 ヘッダ、クォートされた抜粋、署名、MIME パート）

* "ウィキリンク" のグローバル参照の探索と、ウィキ

* 複数の章のファイルを一冊の本に編んだような、複合ドキュメント

* そして、それ以外に見つけたもの

.. _`PEP (Python 拡張提案)`:
.. _PEPs (Python Enhancement Proposals):
   http://www.python.org/peps/pep-0012.html

.. Releases & Snapshots
   ====================

リリース & スナップショット
===========================

.. While we are trying to follow a "release early & often" policy,
   features are added very frequently.  Since the code in the Subversion
   repository is usually in a bug-free state, we recommend that you use
   the current snapshot (which is usually updated within an hour of
   changes being committed to the repository):

私たちは "早く & 頻繁にリリースする" というポリシーに従うように努めていますが、\
新しい機能はしょっちゅう追加されます。Subversion リポジトリの中のコードは通常、\
バグの無い状態なので、現時点でのスナップショット（通常はリポジトリに変更が
コミットされてから１時間以内に更新されます）を使う事をオススメします:

.. * Snapshot of Docutils code, documentation, front-end tools, and
     tests:
     http://docutils.svn.sourceforge.net/viewvc/docutils/trunk/docutils/?view=tar

   * Snapshot of the Sandbox (experimental, contributed code):
     http://docutils.svn.sourceforge.net/viewvc/docutils/trunk/sandbox/?view=tar

* Docutils のコード、ドキュメント、フロントエンドツールおよびテストの
  スナップショット:
  http://docutils.svn.sourceforge.net/viewvc/docutils/trunk/docutils/?view=tar

* Sandbox （実験的なコードや、コントリビューションコード）のスナップショット:
  http://docutils.svn.sourceforge.net/viewvc/docutils/trunk/sandbox/?view=tar

.. To keep up to date on the latest developments, download fresh copies of
   the snapshots regularly or use a working copy of the
   `Subversion repository`_.

最新の動向を保つために、定期的にスナップショットの新しいコピーをダウンロードしたり、
`Subversion リポジトリ`_ の作業コピーを使ってください。

.. _`Subversion リポジトリ`:
.. _Subversion repository: docs/dev/repository.html


.. Requirements
   ============

必要条件
========

.. To run the code, Python_ must be installed.
   Docutils is compatible with Python versions from 2.3 up to 2.7 and
   versions 3.1 and 3.2 (cf. `Python 3 compatibility`_).

コードを実行するには、 Python_ がインストールされていなければなりません。
Docutils は Python のバージョン 2.3 から 2.7 までと、バージョン 3.1 および\
3.2 （cf. `Python_3 互換性`_ ）に互換性があります。

.. Docutils uses the following packages for enhanced functionality, if they are
   installed:

Docutils は、次のモジュールがインストールされていれば、機能性拡張のために
それらを使います:

.. * The `Python Imaging Library`_, or PIL, is used for some image
     manipulation operations.

   * The `Pygments`_ syntax highlighter is used for content of `code`
     directives and roles.

* `Python Imaging ライブラリ`_ または PIL は、画像操作のために使用します。

* `Pygments`_ シンタックスハイライターは、 `code` ディレクティブや
  ロールのコンテンツに使用します。

.. _Python: http://www.python.org/.
.. _`Python Imaging ライブラリ`:
.. _Python Imaging Library: http://www.pythonware.com/products/pil/
.. _Pygments: http://pygments.org/


.. Python 3 compatibility
   ----------------------

Python_3 互換性
---------------

.. The Docutils codebase is written for Python 2 and uses "on-demand"
   translation for `porting to Python 3`_.

Docutils のコードベースは Python_2 用に書かれており、 `Python_3 への移植`_ は
"オンデマンド" の翻訳を用いています。

.. * The `setup.py` script generates Python 3 compatible sources in
     ``build/`` and tests in ``tests3/`` sub-directories during
     installation_ with Python 3.

   * The scripts in the ``tools/`` sub-directory work with all supported
     Python versions without conversion.

   * To convert the sources without installing (e.g. for testing), run
     ``python3 setup.py build``.

   * When editing the source, do changes on the Python 2 versions of the
     files and re-run the build command.

* Python_3 でインストールをする際に、 `setup.py` スクリプトが Python_3 互換の
  ソースを ``build/`` ディレクトリに生成し、 ``test3/`` サブディレクトリ内で
  テストを実行します。

* ``tools`` サブディレクトリの中のスクリプトは、変換することなく、全ての
  サポートされている Python のバージョンで動作します。

* インストールせずにソースを変換（例えばテスト用）するためには、
  ``python3 setup.py build`` を実行します。

* ソースを編集するとき、対象のファイルを Python_2 上で変更し、ビルドコマンドを
  再度実行します。

.. Using Docutils with Python 3.x is less tested and might still have some
   issues.

Python_3.x で Docutils を使うにはテストがあまりされていないですし、まだいくつか
問題があるかも知れません。

.. _`Python_3 への移植`:
.. _porting to Python 3: http://docs.python.org/py3k/howto/pyporting.html


.. Project Files & Directories
   ===========================

プロジェクトのファイルとディレクトリ
====================================

.. * README.txt: You're reading it.

   * COPYING.txt: Public Domain Dedication and copyright details for
     non-public-domain files (most are PD).

   * FAQ.txt: Frequently Asked Questions (with answers!).

   * RELEASE-NOTES.txt: Summary of the major changes in recent releases.

   * HISTORY.txt: A detailed change log, for the current and all previous
     project releases.

   * BUGS.txt: Known bugs, and how to report a bug.

   * THANKS.txt: List of contributors.

   * setup.py: Installation script.  See "Installation" below.

   * install.py: Quick & dirty installation script.  Just run it.  For
     any kind of customization or help though, setup.py must be used.

   * docutils: The project source directory, installed as a Python
     package.

   * docs: The project documentation directory.  Read ``docs/index.txt``
     for an overview.

   * docs/user: The project user documentation directory.  Contains the
     following documents, among others:

     - docs/user/tools.txt: Docutils Front-End Tools
     - docs/user/latex.txt: Docutils LaTeX Writer
     - docs/user/rst/quickstart.txt: A ReStructuredText Primer
     - docs/user/rst/quickref.html: Quick reStructuredText (HTML only)

   * docs/ref: The project reference directory.
     ``docs/ref/rst/restructuredtext.txt`` is the reStructuredText
     reference.

   * licenses: Directory containing copies of license files for
     non-public-domain files.

   * tools: Directory for Docutils front-end tools.  See
     ``docs/user/tools.txt`` for documentation.

   * test: Unit tests.  Not required to use the software, but very useful
     if you're planning to modify it.  See `Running the Test Suite`_
     below.

* README.txt: 今あなたが読んでいるものです。

* COPYING.txt: パブリックドメインの貢献と非パブリックドメインなファイルの\
  著作権表示（ほとんどがパブリックドメイン）です。

* FAQ.txt: よくある質問（とその回答も！）

* RELEASE-NOTES.txt: 最近のリリースでの主要な変更のサマリです。

* HISTORY.txt: 現在と、過去の全てのリリースにおける変更の詳細です。

* BUGS.txt: 既知のバグ、およびバグレポートの仕方です。

* THANKS.txt: コントリビューターの一覧です。

* setup.py: インストレーションスクリプトです。\
  次の "インストレーション" を見てください

* install.py: クイック & ダーティなインストレーションスクリプトです。\
  ただ実行するだけです。何かしらのカスタマイズやヘルプには、setup.py を\
  使う必要があります。

* docutils: Python パッケージとしてインストールされる、プロジェクトの\
  ソースディレクトリです。

* docs: プロジェクトドキュメントのディレクトリです。\
  概要は ``docs/index.txt`` を読んでください。

* docs/user: プロジェクトユーザドキュメントのディレクトリです。\
  とりわけ、次のドキュメントが含まれています:

  - docs/user/tools.txt: Docutils フロントエンドツール
  - docs/user/latex.txt: Docutils LaTeX ライタ
  - docs/user/rst/quickstart.txt: reStructuredText 入門
  - docs/user/rst/quickref.html: 早わかり reStructuredText（HTML のみ）

* docs/ref: プロジェクトリファレンスのディレクトリです。\
  ``docs/ref/rst/restructuredtext.txt`` は reStructuredText のリファレンスです。

* licenses: ディレクトリには非パブリックドメインのファイルのための\
  ライセンスファイルのコピーが含まれています。

* tools: Docutils フロントエンドツールのためのディレクトリです。\
  ドキュメントは ``docs/user/tools.txt`` を参照してください。

* test: ユニットテストです。ソフトウェアを使うためには必要ないですが、\
  変更を行うつもりであれば非常に便利です。\
  下記の `テストスイートの実行`_ を参照してください。

.. Generated directories when installing under Python 3:

Python_3 でインストールする時に生成されるディレクトリ:

.. * build: Converted sources.

   * test3: Converted tests.

* build: 変換されたソースです。

* test3: 変換されたテストです。


.. Installation
   ============

インストレーション
==================

.. The first step is to expand the ``.tgz`` archive in a temporary
   directory (**not** directly in Python's ``site-packages``).  It
   contains a distutils setup file "setup.py".  OS-specific installation
   instructions follow.

最初の一歩は ``.tgz`` アーカイブを一時ディレクトリ（Python の ``site-packages``\
ディレクトリに直接 **入れない** でください）の中に展開することです。
アーカイブには distutils のセットアップファイル "setup.py" を含んでいます。
OS 別のインストレーション手順に続きます。

.. GNU/Linux, BSDs, Unix, Mac OS X, etc.
   -------------------------------------

GNU/Linux, BSD, Unix, Mac OS X など
-----------------------------------

.. 1. Open a shell.

   2. Go to the directory created by expanding the archive::

          cd <archive_directory_path>

   3. Install the package (you may need root permissions to complete this
      step)::

          su
          (enter admin password)
          python setup.py install

      If the python executable isn't on your path, you'll have to specify
      the complete path, such as ``/usr/local/bin/python``.

      To install for a specific Python version, use this version in the
      setup call, e.g. ::

          python3.1 setup.py install

      To install for different Python versions, repeat step 3 for every
      required version. The last installed version will be used in the
      `shebang line`_ of the ``rst2*.py`` wrapper scripts.

1. シェルを開きます。

2. アーカイブを展開してできたディレクトリに移動します ::

       cd <archive_directory_path>

3. パッケージをインストールします（このステップを完了するにはルート権限が\
   必要かも知れません） ::

       su
       (管理者パスワードを入力)
       python setup.py install

   もし python 実行形式が path にない場合、 ``/usr/local/bin/python`` の\
   ように完全なパスを指定しなければなりません。

   特定の Python バージョン用にインストールするには、セットアップの\
   呼び出しでこのバージョンを使います。例えば ::

       python3.1 setup install

   異なる Python のバージョン用にインストールするには、必要なすべての\
   バージョンで手順３を繰り返します。最後にインストールしたバージョンが\
   ``rst2\*.py`` ラッパースクリプトの `シェバン行`_ に使用されます。

   .. _`シェバン行`:
   .. _shebang line: http://en.wikipedia.org/wiki/Shebang_%28Unix%29

Windows
-------

.. Just double-click ``install.py``.  If this doesn't work, try the
   following:

``install.py`` をダブルクリックするだけです。もしこれが動かなかったら、\
次を試してください :

.. 1. Open a DOS Box (Command Shell, MS-DOS Prompt, or whatever they're
      calling it these days).

   2. Go to the directory created by expanding the archive::

          cd <archive_directory_path>

   3. Install the package::

          <path_to_python.exe>\python setup.py install

      To install for a specific python version, specify the Python
      executable for this version.

      To install for different Python versions, repeat step 3 for every
      required version.

1. DOS ボックス（コマンドシェル、MS-DOSプロンプト、もしくはこの頃それらが\
   呼ばれている名前の何か）を開きます。

2. アーカイブを展開してできたディレクトリに移動します ::

       cd <archive_directory_path>

3. パッケージをインストールします ::

       <path_to_python.exe>\python setup.py install

   特定の Python バージョン用にインストールするには、このバージョンの\
   Python 実行形式を指定します。

   異なる Python のバージョン用にインストールするには、必要なすべての\
   バージョンで手順３を繰り返します。

.. Optional steps:

オプションの手順:

.. * `running the test suite`_

   * `converting the documentation`_

* `テストスイートの実行`_

* `ドキュメントの変換`_


.. Usage
   =====

使い方
======

.. There are many front-end tools in the unpacked "tools" subdirectory.
   Installation under Unix places copies in the PATH.
   You may want to begin with the "rst2html.py" front-end tool.  Most
   tools take up to two arguments, the source path and destination path,
   with STDIN and STDOUT being the defaults.  Use the "--help" option to
   the front-end tools for details on options and arguments.  See
   Docutils Front-End Tools (``docs/user/tools.txt``) for full documentation.

解凍した "tools" サブディレクトリにはたくさんのフロントエンドツールがあります。
Unix 環境でのインストレーションでは PATH 上にコピーを配置します。
"rst2html.py" フロントエンドツールから始めたいと思うでしょう。
ほとんどのツールは source path と destination path の２つの引数に、\
デフォルトで STDIN と STDOUT を取ります。オプションや引数の詳細については\
フロントエンドツールの "--help" オプションを使ってください。
すべてのドキュメントは Docutils フロントエンドツール（ ``docs/user/tools.txt`` ）\
を参照してください。

.. The package modules are continually growing and evolving.  The
   ``docutils.statemachine`` module is usable independently.  It contains
   extensive inline documentation (in reStructuredText format of course).

パッケージモジュールは継続的に成長し、進化しています。\
``docutils.statemachine`` モジュールは独立して使用可能で、大規模なインラインの
ドキュメントを含んでいます（もちろん reStructuredText のフォーマットで）。

..
   Contributions are welcome!

貢献は歓迎します！

.. Converting the documentation
   ============================

ドキュメントの変換
==================

.. After unpacking and installing the Docutils package, the following
   shell commands will generate HTML for all included documentation::

Docutils パッケージを展開、インストールした後、次のシェルコマンドによって\
含まれているすべてのドキュメントの HTML が生成されます ::

    cd <archive_directory_path>/tools
    ./buildhtml.py ../

..
   On Windows systems, type::

Windows システムでは、次のとおりにタイプします ::

    cd <archive_directory_path>\tools
    python buildhtml.py ..

.. The final directory name of the ``<archive_directory_path>`` is
   "docutils" for snapshots.  For official releases, the directory may be
   called "docutils-X.Y.Z", where "X.Y.Z" is the release version.
   Alternatively::

``<archive_directory_path>`` の最終的なディレクトリ名は、スナップショットの\
場合は "docutils" です。
公式リリースでは、ディレクトリは "docutils-X.Y.Z" となり、 "X.Y.Z" には\
リリースバージョンが入ります。
別のやり方 ::

    cd <archive_directory_path>
    tools/buildhtml.py --config=tools/docutils.conf          (Unix)
    python tools\buildhtml.py --config=tools\docutils.conf   (Windows)

.. Some files may generate system messages (warnings and errors).  The
   ``docs/user/rst/demo.txt`` file (under the archive directory) contains
   five intentional errors.  (They test the error reporting mechanism!)

いくつかのファイルはシステムメッセージ（警告やエラー）を出すかも知れません。
``docs/user/rst/demo.txt`` ファイル（アーカイブディレクトリ配下）は、\
意図的なエラーを５つ含んでいます（これらはエラー報告メカニズムをテスト\
しています！）

.. Running the Test Suite
   ======================

テストスイートの実行
====================

.. The test suite is documented in `Docutils Testing`_ (docs/dev/testing.txt).

テストスイートは `Docutils テスティング`_ （docs/dev/testing.txt）に
書かれています。

.. To run the entire test suite, open a shell and use the following
   commands::

テストスイート全体を実行するには、シェルを開いて次のコマンドを使います ::

    cd <archive_directory_path>/test
    ./alltests.py

..
   Under Windows, type::

Windows では次のようにタイプします ::

    cd <archive_directory_path>\test
    python alltests.py

..
   For testing with Python 3 use the converted test suite::

Python_3 でのテストには変換されたテストスイートを使います ::

    cd <archive_directory_path>/test3
    python3 alltests.py


.. You should see a long line of periods, one for each test, and then a
   summary like this::

長い区切り線、一つずつのテスト、そしてこのようなサマリが表示されるはずです ::

    Ran 1111 tests in 24.653s

    OK
    Elapsed time: 26.189 seconds

.. The number of tests will grow over time, and the times reported will
   depend on the computer running the tests.  The difference between the
   two times represents the time required to set up the tests (import
   modules, create data structures, etc.).

テストの件数は時間とともに増えるでしょうし、報告される時間はテストを\
実行している計算機に依存するでしょう。
二つの時間の差は、テストのセットアップに掛かる時間を表しています\
（モジュールのインポート、データ構造の作成、等）。

.. If any of the tests fail, please `open a bug report`_, `send email`_,
   or post a message via the `web interface`_ (see `Bugs <BUGS.html>`_).
   Please include all relevant output, information about your operating
   system, Python version, and Docutils version.  To see the Docutils
   version, use one of the ``rst2*`` front ends or ``tools/quicktest.py``
   with the ``--version`` option, e.g.::

いずれかのテストが失敗した場合は、 `バグレポートを開き`_ 、 `メールを送る`_ か、\
もしくは `web インターフェース`_ 経由でメッセージをポストしてください\
（ `Bugs <BUGS.html>`_ を参照してください）。
関連する出力、あなたのオペレーティングシステムに関する情報、Python バージョン、\
Docutils のバージョンをすべて含めてください。Docutils のバージョンを確認する\
ためには、 ``rst2*`` フロントエンドのどれか、または ``tools/quicktest.py`` を\
``--version`` オプションを付けて使います。例えば ::

    cd ../tools
    ./quicktest.py --version

..
   Windows users type these commands::

Windows ユーザは次のコマンドをタイプします ::

    cd ..\tools
    python quicktest.py --version


.. _`Docutils テスティング`:
.. _Docutils Testing: http://docutils.sourceforge.net/docs/dev/testing.html
.. _`バグレポートを開き`:
.. _open a bug report:
   http://sourceforge.net/tracker/?group_id=38414&atid=422030
.. _`メールを送る`:
.. _send email: mailto:docutils-users@lists.sourceforge.net
   ?subject=Test%20suite%20failure
.. _`web インターフェース`:
.. _web interface: http://post.gmane.org/post.php
   ?group=gmane.text.docutils.user&subject=Test+suite+failure


.. Getting Help
   ============

助けを求めるには
================

.. If you have questions or need assistance with Docutils or
   reStructuredText, please post a message to the Docutils-users_ mailing
   list.

Docutils や reStrcuturedText についての質問があったり、支援が必要な場合は、\
`Docutils ユーザーズ`_ メーリングリストにメッセージを送ってください。

.. _`Docutils ユーザーズ`:
.. _Docutils-users: docs/user/mailing-lists.html#docutils-users


..
   Local Variables:
   mode: indented-text
   indent-tabs-mode: nil
   sentence-end-double-space: t
   fill-column: 70
   End:
