# Trend-Trading
TEMA trend trading with 1m candle
<xml xmlns="http://www.w3.org/1999/xhtml" collection="false">
  <block type="after_purchase" id="?:TXa2cX:V#a%Iid!;+U" x="806" y="-46">
    <statement name="AFTERPURCHASE_STACK">
      <block type="controls_if" id="ul.VsfM?uTaN8sxZ^]u7">
        <mutation else="1"></mutation>
        <value name="IF0">
          <block type="contract_check_result" id="qb3=UY~78mIYk]cbMS94">
            <field name="CHECK_RESULT">win</field>
          </block>
        </value>
        <statement name="DO0">
          <block type="math_change" id="F6h3l`Vx+E[%dVC(IwYJ">
            <field name="VAR">Num of Win</field>
            <value name="DELTA">
              <shadow type="math_number" id="@)Cd4:c}Rpr]$fA!=G+e">
                <field name="NUM">1</field>
              </shadow>
            </value>
            <next>
              <block type="variables_set" id="=RTTwHY%Y`bU473w?b|Q">
                <field name="VAR">Num of Lost</field>
                <value name="VALUE">
                  <block type="math_number" id="TE@mGgDPEiKy4^D3zV{~">
                    <field name="NUM">0</field>
                  </block>
                </value>
                <next>
                  <block type="notify" id="F]$/?YiT86m_I{}+~3xb">
                    <field name="NOTIFICATION_TYPE">success</field>
                    <value name="MESSAGE">
                      <block type="text_join" id=":afMZ+O5y6pI##i?_8(A">
                        <mutation items="2"></mutation>
                        <value name="ADD0">
                          <block type="text" id="%L|{7gBz}(}95.ZtZ|5p">
                            <field name="TEXT">Won:</field>
                          </block>
                        </value>
                        <value name="ADD1">
                          <block type="read_details" id="(}viCx~Q-VdY7S5rSu:u">
                            <field name="DETAIL_INDEX">4</field>
                          </block>
                        </value>
                      </block>
                    </value>
                    <next>
                      <block type="variables_set" id="d-U;wl$Rybh?~?KE1=0D">
                        <field name="VAR">Initial Amount</field>
                        <value name="VALUE">
                          <block type="variables_get" id="~O()/Q,-5EbJPvY{SBor">
                            <field name="VAR">Win Amount</field>
                          </block>
                        </value>
                      </block>
                    </next>
                  </block>
                </next>
              </block>
            </next>
          </block>
        </statement>
        <statement name="ELSE">
          <block type="math_change" id="44Ac;tCz(1TQMv/ziz7r">
            <field name="VAR">Num of Lost</field>
            <value name="DELTA">
              <shadow type="math_number" id="eUY3m?MR3Z5pxz]u;lM0">
                <field name="NUM">1</field>
              </shadow>
            </value>
            <next>
              <block type="variables_set" id="swnS=1fxQ,AWfEh0{,Fh">
                <field name="VAR">Num of Win</field>
                <value name="VALUE">
                  <block type="math_number" id="+tajp+14#6yd*{R/I$xQ">
                    <field name="NUM">0</field>
                  </block>
                </value>
                <next>
                  <block type="notify" id="Z/Ofyk^X.[+yF#2X^O@%">
                    <field name="NOTIFICATION_TYPE">warn</field>
                    <value name="MESSAGE">
                      <block type="text_join" id="4S~L4@gH2R}}0{d6YzQR">
                        <mutation items="2"></mutation>
                        <value name="ADD0">
                          <block type="text" id="=x(V.YD#EXb!3q6cr(2/">
                            <field name="TEXT">Lost:</field>
                          </block>
                        </value>
                        <value name="ADD1">
                          <block type="math_single" id="|2NJ^Kf:H[rr59UuwOz`">
                            <field name="OP">ABS</field>
                            <value name="NUM">
                              <shadow type="math_number" id="soB[)@Ez!AUWj@pNv?dU">
                                <field name="NUM">9</field>
                              </shadow>
                              <block type="read_details" id="NB_fXB_QNrrDsU++q26|">
                                <field name="DETAIL_INDEX">4</field>
                              </block>
                            </value>
                          </block>
                        </value>
                      </block>
                    </value>
                    <next>
                      <block type="variables_set" id="^[yUda[S5,DprWu2IHbi">
                        <field name="VAR">last result</field>
                        <value name="VALUE">
                          <block type="text" id="CwP?%]ygL2-aYO;j#)Y^">
                            <field name="TEXT">LOSS</field>
                          </block>
                        </value>
                        <next>
                          <block type="math_change" id="K@ow/j9Dhypt]H~q!D|z">
                            <field name="VAR">Initial Amount</field>
                            <value name="DELTA">
                              <shadow type="math_number" id="fDQsAu}J;X*5KZ}N*^Wi">
                                <field name="NUM">1</field>
                              </shadow>
                              <block type="math_arithmetic" id="fA(Kq_WTB?:2^i3{N5Mv">
                                <field name="OP">MULTIPLY</field>
                                <value name="A">
                                  <shadow type="math_number" id="0(byU7?srIIA}1*GbDm[">
                                    <field name="NUM">1</field>
                                  </shadow>
                                  <block type="math_single" id="*p3UW4yXtoh+c#2P/|{@">
                                    <field name="OP">ABS</field>
                                    <value name="NUM">
                                      <shadow type="math_number" id="6biP%{r..`vb([6_{#[r">
                                        <field name="NUM">9</field>
                                      </shadow>
                                      <block type="read_details" id="}(sQTz-9G:U,{bn!I2;k">
                                        <field name="DETAIL_INDEX">4</field>
                                      </block>
                                    </value>
                                  </block>
                                </value>
                                <value name="B">
                                  <shadow type="math_number" id="C9-,SOUICTigG3EuuA5p">
                                    <field name="NUM">1.1</field>
                                  </shadow>
                                </value>
                              </block>
                            </value>
                            <next>
                              <block type="controls_if" id="+p3T6yrD,=JI$Ldt?k[4">
                                <value name="IF0">
                                  <block type="logic_compare" id="RdMDF[f=@7~(n^w|rO+t">
                                    <field name="OP">GTE</field>
                                    <value name="A">
                                      <block type="math_single" id="U@Cz{e~!=TWP_JxpkpSa">
                                        <field name="OP">ABS</field>
                                        <value name="NUM">
                                          <shadow type="math_number" id="56J^(!%I.Fx2DkrGfm{q">
                                            <field name="NUM">9</field>
                                          </shadow>
                                          <block type="read_details" id="0T}rY_6(TVPgx7_~JHk7">
                                            <field name="DETAIL_INDEX">4</field>
                                          </block>
                                        </value>
                                      </block>
                                    </value>
                                    <value name="B">
                                      <block type="variables_get" id="(?8VPF=~Z_SzB8RLP)GL">
                                        <field name="VAR">Max Loss Amount</field>
                                      </block>
                                    </value>
                                  </block>
                                </value>
                                <statement name="DO0">
                                  <block type="variables_set" id=".k}C]e/^LKz0*(,60|b?">
                                    <field name="VAR">Initial Amount</field>
                                    <value name="VALUE">
                                      <block type="variables_get" id="9uFENU[q|.!g3{e,XR-E">
                                        <field name="VAR">Win Amount</field>
                                      </block>
                                    </value>
                                  </block>
                                </statement>
                              </block>
                            </next>
                          </block>
                        </next>
                      </block>
                    </next>
                  </block>
                </next>
              </block>
            </next>
          </block>
        </statement>
        <next>
          <block type="notify" id="zX2u$OqfR)F^/mVz+,8j">
            <field name="NOTIFICATION_TYPE">info</field>
            <value name="MESSAGE">
              <block type="text_join" id="P4)5|IVwJP=~/?)gsa:i">
                <mutation items="2"></mutation>
                <value name="ADD0">
                  <block type="text" id="Kee7lAK|Me}G$F%2sX!_">
                    <field name="TEXT">Total Profit</field>
                  </block>
                </value>
                <value name="ADD1">
                  <block type="total_profit" id="a)bE_w)x/F}=?wQ(8z1%"></block>
                </value>
              </block>
            </value>
            <next>
              <block type="controls_if" id="*T0du$?uTZJZ4D3E*9?s">
                <mutation elseif="1"></mutation>
                <value name="IF0">
                  <block type="logic_compare" id="D9bEjC8I~.vz_N9lH{T0">
                    <field name="OP">LT</field>
                    <value name="A">
                      <block type="total_profit" id="=eQm2XSw.rYyExEUXjVr"></block>
                    </value>
                    <value name="B">
                      <block type="variables_get" id="ig@yG0`jyxWH6QP!$R|z">
                        <field name="VAR">Expected Profit</field>
                      </block>
                    </value>
                  </block>
                </value>
                <statement name="DO0">
                  <block type="trade_again" id="4@JcI#uIDv~c(PPGio_`"></block>
                </statement>
                <value name="IF1">
                  <block type="logic_compare" id="09xbI)b?+bZ_($~oM`g0">
                    <field name="OP">EQ</field>
                    <value name="A">
                      <block type="total_profit" id="p0)!Pu);zW*:$OwI.GdH"></block>
                    </value>
                    <value name="B">
                      <block type="variables_get" id="KE^;=^{}E#+]0^1PG,$P">
                        <field name="VAR">Expected Profit</field>
                      </block>
                    </value>
                  </block>
                </value>
                <statement name="DO1">
                  <block type="text_print" id="kS:0E.8[k#l_,ofl;r5.">
                    <value name="TEXT">
                      <shadow type="text" id="eZUb-P^OKXwOD]NR4c~?">
                        <field name="TEXT">abc</field>
                      </shadow>
                      <block type="text_join" id="+Wa/G#bE=`+DK0;,_ZBN">
                        <mutation items="2"></mutation>
                        <value name="ADD0">
                          <block type="text" id="2_j]n=}b*JXgR/_Y1TA{">
                            <field name="TEXT">Done! Total profit</field>
                          </block>
                        </value>
                        <value name="ADD1">
                          <block type="total_profit" id="!NQxO^Z;IMww7*=pdEz2"></block>
                        </value>
                      </block>
                    </value>
                  </block>
                </statement>
              </block>
            </next>
          </block>
        </next>
      </block>
    </statement>
  </block>
  <block type="trade" id="h`5gLTr2-]4B1S~yWW:~" x="0" y="0">
    <statement name="SUBMARKET">
      <block type="variables_set" id="lp)!RJq:WEh8`tB6[$UO">
        <field name="VAR">Max Loss Amount</field>
        <value name="VALUE">
          <block type="math_number" id=",X!I8L{MDm2xu=Lj+w{A">
            <field name="NUM">50</field>
          </block>
        </value>
        <next>
          <block type="variables_set" id="kJpr5dD,/as9NNrghle8">
            <field name="VAR">Expected Profit</field>
            <value name="VALUE">
              <block type="math_number" id="sTW}1C?JANi#dfrM9etn">
                <field name="NUM">100</field>
              </block>
            </value>
            <next>
              <block type="variables_set" id="4(A4MV1{:lqz4u5NmTAh">
                <field name="VAR">Win Amount</field>
                <value name="VALUE">
                  <block type="math_number" id="Ck#U+#|]Up:;|*Ayl2VK">
                    <field name="NUM">0.5</field>
                  </block>
                </value>
                <next>
                  <block type="variables_set" id="C59z|1j4aGtzhs8t{wJN">
                    <field name="VAR">Initial Amount</field>
                    <value name="VALUE">
                      <block type="math_number" id="]QU.[)#-ngdst,IQQA4I">
                        <field name="NUM">0.5</field>
                      </block>
                    </value>
                    <next>
                      <block type="variables_set" id="5Ct#NHhJ36[nqLv=|3Hs">
                        <field name="VAR">WIN RATE</field>
                        <value name="VALUE">
                          <block type="math_number" id="ftlgLtzr[YZ,b,sf6.8Q">
                            <field name="NUM">1.5</field>
                          </block>
                        </value>
                        <next>
                          <block type="variables_set" id="ccxN6+;HOQIbwd-KHb#b">
                            <field name="VAR">Lost Rate</field>
                            <value name="VALUE">
                              <block type="math_number" id="QWMr)r3wEm72s}9u6C2l">
                                <field name="NUM">1</field>
                              </block>
                            </value>
                            <next>
                              <block type="market" id="JDTjhA[jS6Tho{Io5:K%">
                                <field name="MARKET_LIST">volidx</field>
                                <field name="SUBMARKET_LIST">random_index</field>
                                <field name="SYMBOL_LIST">R_100</field>
                                <field name="TRADETYPECAT_LIST">callput</field>
                                <field name="TRADETYPE_LIST">risefall</field>
                                <field name="TYPE_LIST">both</field>
                                <field name="CANDLEINTERVAL_LIST">60</field>
                                <field name="DURATIONTYPE_LIST">t</field>
                                <field name="PAYOUTTYPE_LIST">stake</field>
                                <field name="CURRENCY_LIST">USD</field>
                                <field name="RESTARTONERROR">TRUE</field>
                                <value name="DURATION">
                                  <block type="math_number" id="uYn`M-g?KTby)Bh,=aQb">
                                    <field name="NUM">5</field>
                                  </block>
                                </value>
                                <value name="AMOUNT">
                                  <block type="variables_get" id="H.m3eBXvRZjOTn7I6TUf">
                                    <field name="VAR">Initial Amount</field>
                                  </block>
                                </value>
                              </block>
                            </next>
                          </block>
                        </next>
                      </block>
                    </next>
                  </block>
                </next>
              </block>
            </next>
          </block>
        </next>
      </block>
    </statement>
  </block>
  <block type="before_purchase" id="b)rH..hM4k2wwH:.7gLG" x="-7" y="376">
    <statement name="BEFOREPURCHASE_STACK">
      <block type="variables_set" id="^75]Vx^7l$hT+7ij?]TJ">
        <field name="VAR">ema_5</field>
        <value name="VALUE">
          <block type="ema" id="d20nm{r%46KXy_79t6AR">
            <value name="INPUT">
              <block type="ohlc_values" id="zyRYG{Ze)kH}J}KXmpnj">
                <field name="OHLCFIELD_LIST">close</field>
              </block>
            </value>
            <value name="PERIOD">
              <block type="math_number" id="?9I0xT9sWNH?ngve,?Wb">
                <field name="NUM">5</field>
              </block>
            </value>
          </block>
        </value>
        <next>
          <block type="variables_set" id="_XE1tu.idcV8ZDOA]0ut">
            <field name="VAR">ema_10</field>
            <value name="VALUE">
              <block type="ema" id="1y{Gk:hg#;W*p`v4~Eu^">
                <value name="INPUT">
                  <block type="ohlc_values" id="+hYwkOkV!9H}K?LJ.6=)">
                    <field name="OHLCFIELD_LIST">close</field>
                  </block>
                </value>
                <value name="PERIOD">
                  <block type="math_number" id="~}Fp}Ut.-7J08/SEAK3U">
                    <field name="NUM">10</field>
                  </block>
                </value>
              </block>
            </value>
            <next>
              <block type="variables_set" id="b{`_#5FO$B$.%D,0YPL!">
                <field name="VAR">ema_21</field>
                <value name="VALUE">
                  <block type="ema" id=":e#lI-(YcAn*XAj|An*O">
                    <value name="INPUT">
                      <block type="ohlc_values" id="/{sJW_wzuw#~iDqUj;*m">
                        <field name="OHLCFIELD_LIST">close</field>
                      </block>
                    </value>
                    <value name="PERIOD">
                      <block type="math_number" id="jf4^%7NiMBckmC|)2fI$">
                        <field name="NUM">21</field>
                      </block>
                    </value>
                  </block>
                </value>
                <next>
                  <block type="variables_set" id=":qe37pG%XxplVVJ^(A2(">
                    <field name="VAR">tema_5</field>
                    <value name="VALUE">
                      <block type="ema" id="onLr:]z]7S__0G9=c[ss">
                        <value name="INPUT">
                          <block type="ticks" id=":cVJ?f^uqWqLjtGLC@tS"></block>
                        </value>
                        <value name="PERIOD">
                          <block type="math_number" id="u?C4Y@3N]RO/eX;~TaO0">
                            <field name="NUM">5</field>
                          </block>
                        </value>
                      </block>
                    </value>
                    <next>
                      <block type="variables_set" id="ld+MPE!CgzhYxG6f?b.X">
                        <field name="VAR">tema_10</field>
                        <value name="VALUE">
                          <block type="ema" id="fNz$hX`Ze;8*FBXD.R8h">
                            <value name="INPUT">
                              <block type="ticks" id="D;)$d6.Fl8]w1J}]9JD)"></block>
                            </value>
                            <value name="PERIOD">
                              <block type="math_number" id="@+HPYW7Wts%p6K(Ol*6-">
                                <field name="NUM">10</field>
                              </block>
                            </value>
                          </block>
                        </value>
                        <next>
                          <block type="variables_set" id="2dE?7Ge9XA-Yxgu,:Fnz">
                            <field name="VAR">tema_21</field>
                            <value name="VALUE">
                              <block type="ema" id="pI!5JpZ*$;BQ(lS~G`mV">
                                <value name="INPUT">
                                  <block type="ticks" id="P:9zZq6-u=agw-fP-f=Y"></block>
                                </value>
                                <value name="PERIOD">
                                  <block type="math_number" id="37i(!t5xQQK]D+Nc;VaG">
                                    <field name="NUM">21</field>
                                  </block>
                                </value>
                              </block>
                            </value>
                            <next>
                              <block type="controls_if" id="E#74dTsh%%;%q-3p|Ggd">
                                <value name="IF0">
                                  <block type="logic_operation" id="$g`K1vp$}?g;-OxFDU[v">
                                    <field name="OP">AND</field>
                                    <value name="A">
                                      <block type="logic_compare" id="?Qx^q8RJQm3O-0+tZc4C">
                                        <field name="OP">GT</field>
                                        <value name="A">
                                          <block type="read_ohlc" id="lLaOkwXCS-H,}Kv5@GYq">
                                            <field name="OHLCFIELD_LIST">high</field>
                                            <value name="CANDLEINDEX">
                                              <block type="math_number" id="G[^OBr0=y/`w]hF1nO(V">
                                                <field name="NUM">2</field>
                                              </block>
                                            </value>
                                          </block>
                                        </value>
                                        <value name="B">
                                          <block type="read_ohlc" id="(xE_|!WwChRboQxcP|?c">
                                            <field name="OHLCFIELD_LIST">high</field>
                                            <value name="CANDLEINDEX">
                                              <block type="math_number" id="t1M%H2.d5{~voqIu3)[=">
                                                <field name="NUM">3</field>
                                              </block>
                                            </value>
                                          </block>
                                        </value>
                                      </block>
                                    </value>
                                    <value name="B">
                                      <block type="logic_compare" id="rC5khU/:ZtK|(!9mEuqC">
                                        <field name="OP">GT</field>
                                        <value name="A">
                                          <block type="read_ohlc" id="ETk#fkM9Nd9CeuxK.$Ez">
                                            <field name="OHLCFIELD_LIST">low</field>
                                            <value name="CANDLEINDEX">
                                              <block type="math_number" id="MjZ1$Vd.L#v+8lSs)^RY">
                                                <field name="NUM">2</field>
                                              </block>
                                            </value>
                                          </block>
                                        </value>
                                        <value name="B">
                                          <block type="read_ohlc" id="yk,=s}!nCtdw];Lo@xM2">
                                            <field name="OHLCFIELD_LIST">low</field>
                                            <value name="CANDLEINDEX">
                                              <block type="math_number" id="4m-w!%4:|:3asrcq-pT:">
                                                <field name="NUM">3</field>
                                              </block>
                                            </value>
                                          </block>
                                        </value>
                                      </block>
                                    </value>
                                  </block>
                                </value>
                                <statement name="DO0">
                                  <block type="controls_if" id="+L0.Mmn=XigX_@,Y!o_]">
                                    <value name="IF0">
                                      <block type="logic_operation" id="sWGRB.wxGB{rda2|#!Lg">
                                        <field name="OP">AND</field>
                                        <value name="A">
                                          <block type="logic_compare" id="oLjrM.;Hn3(_$rVIFiF:">
                                            <field name="OP">GT</field>
                                            <value name="A">
                                              <block type="variables_get" id="YGc#gu`$p7.mH#zla^CV">
                                                <field name="VAR">ema_5</field>
                                              </block>
                                            </value>
                                            <value name="B">
                                              <block type="variables_get" id="VkH/GFm5;-jibmoC@a2h">
                                                <field name="VAR">ema_10</field>
                                              </block>
                                            </value>
                                          </block>
                                        </value>
                                        <value name="B">
                                          <block type="logic_compare" id="G?T|i{(BtzBgupZ0GI:O">
                                            <field name="OP">GT</field>
                                            <value name="A">
                                              <block type="read_ohlc" id="tOkeF%m.26)l~Wn]b-^:">
                                                <field name="OHLCFIELD_LIST">close</field>
                                              </block>
                                            </value>
                                            <value name="B">
                                              <block type="read_ohlc" id="I{3g}nJyd]hWH)`:Wdd_">
                                                <field name="OHLCFIELD_LIST">low</field>
                                                <value name="CANDLEINDEX">
                                                  <block type="math_number" id="NEfM@9JJs]OVK_/U6)3|">
                                                    <field name="NUM">2</field>
                                                  </block>
                                                </value>
                                              </block>
                                            </value>
                                          </block>
                                        </value>
                                      </block>
                                    </value>
                                    <statement name="DO0">
                                      <block type="controls_if" id="61x3u[hRqcYWzA~kHt/_">
                                        <value name="IF0">
                                          <block type="logic_operation" id="mAtQONuU/FE$1HP#GCUa">
                                            <field name="OP">AND</field>
                                            <value name="A">
                                              <block type="logic_compare" id="{-%+gl$MukOWY#kk_H:w">
                                                <field name="OP">GT</field>
                                                <value name="A">
                                                  <block type="variables_get" id=":$_Pj9usoH#(hhiKZiiD">
                                                    <field name="VAR">tema_5</field>
                                                  </block>
                                                </value>
                                                <value name="B">
                                                  <block type="variables_get" id="rpGbE~79LhW/[5-DLcge">
                                                    <field name="VAR">tema_10</field>
                                                  </block>
                                                </value>
                                              </block>
                                            </value>
                                            <value name="B">
                                              <block type="logic_compare" id="!DJE^M5#?cBJDdGfSUB?">
                                                <field name="OP">GT</field>
                                                <value name="A">
                                                  <block type="variables_get" id="+`W?44`v=tL|U|}yqd/{">
                                                    <field name="VAR">tema_10</field>
                                                  </block>
                                                </value>
                                                <value name="B">
                                                  <block type="variables_get" id="}SCmrAmZQ{ah5IyRC_G1">
                                                    <field name="VAR">tema_21</field>
                                                  </block>
                                                </value>
                                              </block>
                                            </value>
                                          </block>
                                        </value>
                                        <statement name="DO0">
                                          <block type="controls_if" id="t/Li.g:Tosm_^:WBI[Hj">
                                            <value name="IF0">
                                              <block type="logic_compare" id="q1y3`O1Vr-Y~1V3:)r^c">
                                                <field name="OP">LT</field>
                                                <value name="A">
                                                  <block type="tick" id="sK^*8mQWIdKL4:1QN_CK"></block>
                                                </value>
                                                <value name="B">
                                                  <block type="variables_get" id="dAG`0omFD-/COmGFm{[/">
                                                    <field name="VAR">tema_5</field>
                                                  </block>
                                                </value>
                                              </block>
                                            </value>
                                            <statement name="DO0">
                                              <block type="purchase" id=";I2|,??afq#)HEkF3]*u">
                                                <field name="PURCHASE_LIST">CALL</field>
                                              </block>
                                            </statement>
                                          </block>
                                        </statement>
                                      </block>
                                    </statement>
                                  </block>
                                </statement>
                                <next>
                                  <block type="controls_if" id="eYc,bEb:%!D5W`|%;V6T">
                                    <value name="IF0">
                                      <block type="logic_operation" id="e/+pc[`er|yy}cp_B3:!">
                                        <field name="OP">AND</field>
                                        <value name="A">
                                          <block type="logic_compare" id="dL!9Xpi1Tv1G6FQ(F`.N">
                                            <field name="OP">LT</field>
                                            <value name="A">
                                              <block type="read_ohlc" id="_%]ADQ8cR[:zK]{C`4[;">
                                                <field name="OHLCFIELD_LIST">high</field>
                                                <value name="CANDLEINDEX">
                                                  <block type="math_number" id="_~*|9sL=w3x/#?#Z5uUt">
                                                    <field name="NUM">2</field>
                                                  </block>
                                                </value>
                                              </block>
                                            </value>
                                            <value name="B">
                                              <block type="read_ohlc" id="?1}cpk80cVX+vt9jOv1]">
                                                <field name="OHLCFIELD_LIST">high</field>
                                                <value name="CANDLEINDEX">
                                                  <block type="math_number" id="d@hvsSpD^h5BbT$4oM+=">
                                                    <field name="NUM">3</field>
                                                  </block>
                                                </value>
                                              </block>
                                            </value>
                                          </block>
                                        </value>
                                        <value name="B">
                                          <block type="logic_compare" id="ZSzwH2KR?;LpvB3pOe83">
                                            <field name="OP">LT</field>
                                            <value name="A">
                                              <block type="read_ohlc" id="p(AFi{R++-Qwhh^NYN0M">
                                                <field name="OHLCFIELD_LIST">low</field>
                                                <value name="CANDLEINDEX">
                                                  <block type="math_number" id="b8^]fiEVFb61nva4UEMc">
                                                    <field name="NUM">2</field>
                                                  </block>
                                                </value>
                                              </block>
                                            </value>
                                            <value name="B">
                                              <block type="read_ohlc" id="n?V.`vDhO+8|{=;rm:ai">
                                                <field name="OHLCFIELD_LIST">low</field>
                                                <value name="CANDLEINDEX">
                                                  <block type="math_number" id="*lfNwFEl=01mVC-+#B7b">
                                                    <field name="NUM">3</field>
                                                  </block>
                                                </value>
                                              </block>
                                            </value>
                                          </block>
                                        </value>
                                      </block>
                                    </value>
                                    <statement name="DO0">
                                      <block type="controls_if" id="}o=BVNB0LTg~MyftH!Xb">
                                        <value name="IF0">
                                          <block type="logic_operation" id="NNnYZ)6rr!8sCT/!|Wms">
                                            <field name="OP">AND</field>
                                            <value name="A">
                                              <block type="logic_compare" id="OvWy!ddQil{?pfRh7Fy~">
                                                <field name="OP">LT</field>
                                                <value name="A">
                                                  <block type="variables_get" id="$EB$fJ;pckmj0YoFLcB/">
                                                    <field name="VAR">ema_5</field>
                                                  </block>
                                                </value>
                                                <value name="B">
                                                  <block type="variables_get" id="SQ@VS%M`t[sXBjUH,Zys">
                                                    <field name="VAR">ema_10</field>
                                                  </block>
                                                </value>
                                              </block>
                                            </value>
                                            <value name="B">
                                              <block type="logic_compare" id="t!;6AzfrUG$U2xCi(D#-">
                                                <field name="OP">LT</field>
                                                <value name="A">
                                                  <block type="read_ohlc" id="8%-;FMHxnm6}RcTd#1*`">
                                                    <field name="OHLCFIELD_LIST">close</field>
                                                  </block>
                                                </value>
                                                <value name="B">
                                                  <block type="read_ohlc" id="=DDc[M]+DN*{{UHKP=RH">
                                                    <field name="OHLCFIELD_LIST">high</field>
                                                    <value name="CANDLEINDEX">
                                                      <block type="math_number" id="+AwAw3lX2A=]g~L;E|D,">
                                                        <field name="NUM">2</field>
                                                      </block>
                                                    </value>
                                                  </block>
                                                </value>
                                              </block>
                                            </value>
                                          </block>
                                        </value>
                                        <statement name="DO0">
                                          <block type="controls_if" id=";zc^.r(;x]ZmS!|g.2au">
                                            <value name="IF0">
                                              <block type="logic_operation" id="c[6jh]}4V]a*HO8Y5WPa">
                                                <field name="OP">AND</field>
                                                <value name="A">
                                                  <block type="logic_compare" id="6^Vty;TV+nboQ$Bj!?DU">
                                                    <field name="OP">LT</field>
                                                    <value name="A">
                                                      <block type="variables_get" id="-rgi:kJfxfuMaOj:B81g">
                                                        <field name="VAR">tema_5</field>
                                                      </block>
                                                    </value>
                                                    <value name="B">
                                                      <block type="variables_get" id="xXc(THbTb`Q[,Z{MPb.9">
                                                        <field name="VAR">tema_10</field>
                                                      </block>
                                                    </value>
                                                  </block>
                                                </value>
                                                <value name="B">
                                                  <block type="logic_compare" id="++l~8]!VTp4tzGc]#%Hu">
                                                    <field name="OP">LT</field>
                                                    <value name="A">
                                                      <block type="variables_get" id="q%.V@d-R|,Vl@iqX|d|(">
                                                        <field name="VAR">tema_10</field>
                                                      </block>
                                                    </value>
                                                    <value name="B">
                                                      <block type="variables_get" id="K|?!{i@ApW8?[Q%34sdH">
                                                        <field name="VAR">tema_21</field>
                                                      </block>
                                                    </value>
                                                  </block>
                                                </value>
                                              </block>
                                            </value>
                                            <statement name="DO0">
                                              <block type="controls_if" id="nZr.b={U8]4I35}[YJ7`">
                                                <value name="IF0">
                                                  <block type="logic_compare" id="omuFE6NO+@l-wl#Lob*W">
                                                    <field name="OP">GT</field>
                                                    <value name="A">
                                                      <block type="tick" id="9SJ}=dY+yEN@4AF4]=#3"></block>
                                                    </value>
                                                    <value name="B">
                                                      <block type="variables_get" id="3J]u.lkgRSZh%;(@AM7o">
                                                        <field name="VAR">tema_5</field>
                                                      </block>
                                                    </value>
                                                  </block>
                                                </value>
                                                <statement name="DO0">
                                                  <block type="purchase" id="c?5CbM4+N?@?op6^rO{_">
                                                    <field name="PURCHASE_LIST">PUT</field>
                                                  </block>
                                                </statement>
                                              </block>
                                            </statement>
                                          </block>
                                        </statement>
                                      </block>
                                    </statement>
                                  </block>
                                </next>
                              </block>
                            </next>
                          </block>
                        </next>
                      </block>
                    </next>
                  </block>
                </next>
              </block>
            </next>
          </block>
        </next>
      </block>
    </statement>
  </block>
</xml>
