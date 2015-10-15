SubversionリポジトリをMercurialリポジトリに変換する
============================================================

`hg convert` で履歴込みで変換できる。

事前準備
------------------------------------------------------------

convert拡張有効化
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Mercurialでconvert拡張が使えるようにしておく。 :file:`~/.hgrc` に以下の行を追加。

.. code-block:: ini

  [extensions]
  hgext.convert=


変換
------------------------------------------------------------

以下のコマンドを実行するとSubversionリポジトリ(:file:`path/to/svnrepo/`)からMercurialリポジトリ(:file:`/path/to/newrepo`)が作成される。

.. code-block:: shell

  hg convert --source-type svn file:///path/to/svnrepo/ /path/to/newrepo
