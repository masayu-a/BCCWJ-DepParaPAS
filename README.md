# BCCWJ-DepParaPAS version 3.3.0_1.2.0_20200601
Syntactic and semantic relation annotation on BCCWJ
## Files and directories
- README.md	this file
- AUTHORS	author of this package
- ChangeLog	change log
- COPYING	copyright
- NEWS	version history
- ntc/	the data -- NAIST Text Corpus formatted   (available via NINJAL server)
- cabocha/ the data -- Extended CaboCha formatted  (available via NINJAL server)
- doc/	documents and papers

## Licence
The annotations of BCCWJ-DepParaPAS are under Creative Commons Attiribution 4.0 International (CC BY 4.0) 
http://creativecommons.org/licenses/by/4.0/
Check the COPYING and AUTHORS files.

However, the original texts of BCCWJ are not under Creative Commons Licence.
For example, the use of PN (NewsPaper) samples are prohibitted for any commercial use.

## Citation
Whenever you refer to this resource, you must cite all of the following five manuscripts.

### MLA Styles
- Syntactic Dependency and Coordination Structure
浅原正幸，松本裕治. "『現代日本語書き言葉均衡コーパス』に対する係り受け・並列構造アノテーション." 言語処理学会第19回年次大会発表論文集 (2013): 66-69.

http://www.anlp.jp/proceedings/annual_meeting/2013/pdf_dir/X1-2.pdf

- Sentence Segmentation
小西光ほか. "BCCWJ 係り受け関係アノテーション付与のための文境界再認定." 第3回コーパス日本語学ワークショップ予稿集 (2013): 135-142.

https://www.ninjal.ac.jp/event/specialists/project-meeting/files/JCLWorkshop_no3_papers/JCLWorkshop_No3_18.pdf

- BCCWJ Original Data
Maekawa, Kikuo, et al. "Balanced corpus of contemporary written Japanese." Language Resources and Evaluation 2.48 (2014): 345-371.

http://link.springer.com/article/10.1007/s10579-013-9261-0

- Semantic Dependency and Coreference Information
植田禎子ほか. "『現代日本語書き言葉均衡コーパス』に対する述語項構造・アノテーション." 第8回コーパス日本語学ワークショップ予稿集 (2015): 205-214.

- the Resource
浅原正幸，大村舞，松本裕治．"BCCWJ-DepParaPAS: 『現代日本語書き言葉均衡コーパス』依存構造アノテーションの重ね合わせ." 言語処理学会第22回年次大会発表論文集 (2016): (To Appear).

### BibTeX
    % Syntactic Dependency and Coordination Structure
    @inProceedings{浅原正幸2013bccwj,
     title={『現代日本語書き言葉均衡コーパス』に対する係り受け・並列構造アノテーション},
     author={浅原 正幸 and 松本 裕治},
     booktitle = {言語処理学会第19回年次大会発表論文集},
     pages = 	 {66--69},
     year = 	 {2013}
    }
    
    % Sentence Segmentation
    @inProceedings{小西光2013bccwj,
      title={BCCWJ 係り受け関係アノテーション付与のための文境界再認定},
      author={小西光 and 小山田由紀 and 浅原正幸 and 柏野 和佳子 and 前川喜久雄},
      booktitle = {第3回コーパス日本語学ワークショップ予稿集},
      pages = 	 {135--142},
      year = 	 {2013},
      organization = {国立国語研究所}
    }
    
    % BCCWJ Original Data
    @article{maekawa2014balanced,
      title={Balanced corpus of contemporary written Japanese},
      author={MAEKAWA, Kikuo and YAMAZAKI, Makoto and OGISO, Toshinobu and MARUYAMA, Takehiko and OGURA, Hideki and KASHINO, Wakako and KOISO, Hanae and YAMAGUCHI, Masaya and TANAKA, Makiro and DEN, Yasuharu},
      journal={Language resources and evaluation},
      volume={48},
      number={2},
      pages={345--371},
      year={2014},
      publisher={Springer}
    }
    
    % Semantic Dependency and Coreference Information
    @inProceedings{植田禎子2015bccwj,
      title={『現代日本語書き言葉均衡コーパス』に対する述語項構造・アノテーション},
      author={植田禎子 and 飯田龍 and 浅原正幸 and 松本裕治 and 徳永健伸},
      booktitle = {第8回コーパス日本語学ワークショップ予稿集},
      pages = 	 {205--214},
      year = 	 {2015},
      organization = {国立国語研究所}
    }
    
    % the Resource
    @inProceedings{浅原正幸2016bccwj,
      title={BCCWJ-DepParaPAS: 『現代日本語書き言葉均衡コーパス』依存構造アノテーションの重ね合わせ},
      author={浅原 正幸 and 大村 舞 and 松本 裕治},
      booktitle = {言語処理学会第22回年次大会発表論文集},
      pages = 	 {489--492},
      year = 	 {2016}
    }

## ファイル形式

- #! DOC 行 ＜文番号＞
- #! DOCID 行
  - ＜ID＞ 文番号
  - ＜newdoc_id＞ 元の newdoc id (PUD のみ)
  - ＜sent_id＞ 元の sent id
  - ＜text＞ 元の text
  - ＜english_text＞ 元の english_text
  - ＜non_projective＞ 交差ありか否か
  - ＜Dynagon_corpusName＞ 国語研所内サーバにおけるデータベース名
  - ＜Dynagon_file＞ 国語研所内サーバにおけるファイル名
  - ＜Dynagon_start＞ 国語研所内サーバにおけるオフセット値

- 係り受け情報行
  - 文節ID
  - 係り先文節ID
  - 係り受け関係ラベル
  - 自立語主辞オフセット（要修正）
  - 付属語主辞オフセット（要修正）
  - SVM 出力値（要修正）

- EOS 行
  - EOS のみからなる文末情報

- 形態素行（タブ区切り）

  - 1列目：出現形

  - 2列目：短単位形態論情報（コンマ区切り）= MeCab-UniDic の出力と同等

    - (0):  pos1
    - (1):  pos2
    - (2):  pos3
    - (3):  pos4
    - (4):  cType
    - (5):  cForm
    - (6):  lForm
    - (7):  lemma
    - (8):  orth
    - (9):  pron
    - (10): orthBase
    - (11): pronBase
    - (12): goshu
    - (13): iType
    - (14): iForm
    - (15): fType
    - (16): fForm
    - (17): iConType
    - (18): fConType
    - (19): type
    - (20): kana
    - (21): kanaBase
    - (22): form
    - (23): formBase
    - (24): aType
    - (25): aConType
    - (26): aModType
    - (27): lid
    - (28): lemma_id

  - 3列目：長単位書字形出現形

  - 4列目：長単位形態論情報（コンマ区切り）

    - (0):  l_pos1
    - (1):  l_pos2
    - (2):  l_pos3
    - (3):  l_pos4
    - (4):  l_cType
    - (5):  l_cForm
    - (6):  l_reading
    - (7):  l_lemma

  - 5列目：文節境界情報

  - 6列目：述語項構造・共参照情報（ntc/のみ）
  
