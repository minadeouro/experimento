<xml xmlns="http://www.w3.org/1999/xhtml" collection="true">
  <variables>
    <variable type="" id="gy-(OQo2ivS$$4TQ+tcJ">Max Loss Amount</variable>
    <variable type="" id="mvV%E7GK^7Cx=BCxt/+N">spot4</variable>
    <variable type="" id="$+4YB1~jnlepPV+/}y+j">Expected Profit</variable>
    <variable type="" id="O~AXmG3`h:n`-WoDm)0~">Initial Amount</variable>
    <variable type="" id="V/`@i2l^h%BA/vg3V?Y_">spot3</variable>
    <variable type="" id="7iAq]Co?H(SF+qm5jgmD">Win Amount</variable>
    <variable type="" id="R]}XJg8*ocRP#{pv/]hP">spot2</variable>
    <variable type="" id="x{5)(}]`;Pr%_}EXY9BW">spot1</variable>
    <variable type="" id="hKa[y{d-7SuUKfxML}Ib">RSI 2</variable>
    <variable type="" id="c,Ra=i;B*t9dXw#@K)lR">RSI</variable>
  </variables>
  <block type="trade" id="73vWdDagX-YhN)CtN.3D" x="0" y="0">
    <field name="MARKET_LIST">volidx</field>
    <field name="SUBMARKET_LIST">random_index</field>
    <field name="SYMBOL_LIST">R_10</field>
    <field name="TRADETYPECAT_LIST">callput</field>
    <field name="TRADETYPE_LIST">risefall</field>
    <field name="TYPE_LIST">both</field>
    <field name="CANDLEINTERVAL_LIST">60</field>
    <field name="TIME_MACHINE_ENABLED">FALSE</field>
    <field name="RESTARTONERROR">TRUE</field>
    <statement name="INITIALIZATION">
      <block type="variables_set" id="XDMYoip}{3uMJ$~,Wa(K">
        <field name="VAR" id="gy-(OQo2ivS$$4TQ+tcJ" variabletype="">Max Loss Amount</field>
        <value name="VALUE">
          <block type="math_number" id="P!2=P_+S,MKLQTjA]xg(">
            <field name="NUM">48</field>
          </block>
        </value>
        <next>
          <block type="variables_set" id="dqduY+F]dYVC%/;)_QyX">
            <field name="VAR" id="$+4YB1~jnlepPV+/}y+j" variabletype="">Expected Profit</field>
            <value name="VALUE">
              <block type="math_number" id="pGL%0jCRlD;R_i-Q:?jz">
                <field name="NUM">50</field>
              </block>
            </value>
            <next>
              <block type="variables_set" id="cG;6qVzC4dU[J9h%wYdK">
                <field name="VAR" id="7iAq]Co?H(SF+qm5jgmD" variabletype="">Win Amount</field>
                <value name="VALUE">
                  <block type="math_number" id="?UMlJ9?s?=7*h-CIL?Hv">
                    <field name="NUM">0.35</field>
                  </block>
                </value>
                <next>
                  <block type="variables_set" id="(GqO!$8|aP4T+(5lW(^E">
                    <field name="VAR" id="O~AXmG3`h:n`-WoDm)0~" variabletype="">Initial Amount</field>
                    <value name="VALUE">
                      <block type="math_number" id="dI_3Be9-$EK_$F=d.7w#">
                        <field name="NUM">0.35</field>
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
    <statement name="SUBMARKET">
      <block type="tradeOptions" id="MgRtLy!`#cD%K?44{Ff9">
        <field name="DURATIONTYPE_LIST">t</field>
        <field name="CURRENCY_LIST">USD</field>
        <value name="DURATION">
          <block type="math_number" id="0p-bjjEuB1k(LNWLaiS]">
            <field name="NUM">5</field>
          </block>
        </value>
        <value name="AMOUNT">
          <block type="variables_get" id="p+TPBS;7,b0?9`GtSOmc">
            <field name="VAR" id="O~AXmG3`h:n`-WoDm)0~" variabletype="">Initial Amount</field>
          </block>
        </value>
      </block>
    </statement>
  </block>
  <block type="before_purchase" id="tOc)]Xd=cAm0aiy+-8(8" x="0" y="346">
    <statement name="BEFOREPURCHASE_STACK">
      <block type="variables_set" id="1@I-41Oe;`a1+,NVY/7l">
        <field name="VAR" id="mvV%E7GK^7Cx=BCxt/+N" variabletype="">spot4</field>
        <value name="VALUE">
          <block type="lists_getIndex" id="2NJ!jNDVf)q)J5:4h)))">
            <mutation statement="false" at="true"></mutation>
            <field name="MODE">GET</field>
            <field name="WHERE">FROM_END</field>
            <value name="VALUE">
              <block type="ticks" id="1i5z+B=vz,}S.F8Sobas"></block>
            </value>
            <value name="AT">
              <block type="math_number" id=")(Aa?q8O4|S3tHGBL{nA">
                <field name="NUM">4</field>
              </block>
            </value>
          </block>
        </value>
        <next>
          <block type="variables_set" id=";QniLKQ$v?%4rMG63dD`">
            <field name="VAR" id="V/`@i2l^h%BA/vg3V?Y_" variabletype="">spot3</field>
            <value name="VALUE">
              <block type="lists_getIndex" id="GqfrN*?,z7$YTb}y$L%0">
                <mutation statement="false" at="true"></mutation>
                <field name="MODE">GET</field>
                <field name="WHERE">FROM_END</field>
                <value name="VALUE">
                  <block type="ticks" id="/2o,kT05/x+}#*G_OK{@"></block>
                </value>
                <value name="AT">
                  <block type="math_number" id="Ferl+p1(i~g|!D3]2*S-">
                    <field name="NUM">3</field>
                  </block>
                </value>
              </block>
            </value>
            <next>
              <block type="variables_set" id="l*=I/OU9M;vm!fgVYYA5">
                <field name="VAR" id="R]}XJg8*ocRP#{pv/]hP" variabletype="">spot2</field>
                <value name="VALUE">
                  <block type="lists_getIndex" id="WMhdh?;hdUWw/f:Qs/P#">
                    <mutation statement="false" at="true"></mutation>
                    <field name="MODE">GET</field>
                    <field name="WHERE">FROM_END</field>
                    <value name="VALUE">
                      <block type="ticks" id="GZa6Y,r$|alkE?B)#eQ2"></block>
                    </value>
                    <value name="AT">
                      <block type="math_number" id="mB,@p4xoChtDx5}5]fx0">
                        <field name="NUM">2</field>
                      </block>
                    </value>
                  </block>
                </value>
                <next>
                  <block type="variables_set" id="eSuM.e}/o7z!q6:5Or`8">
                    <field name="VAR" id="x{5)(}]`;Pr%_}EXY9BW" variabletype="">spot1</field>
                    <value name="VALUE">
                      <block type="lists_getIndex" id="!AbYu5h,9S02M3G+/oZu">
                        <mutation statement="false" at="true"></mutation>
                        <field name="MODE">GET</field>
                        <field name="WHERE">FROM_END</field>
                        <value name="VALUE">
                          <block type="ticks" id="vc?NR8e8a2N:o[?(KvuW"></block>
                        </value>
                        <value name="AT">
                          <block type="math_number" id="rVUzFj4aNGmK/D9swzhw">
                            <field name="NUM">1</field>
                          </block>
                        </value>
                      </block>
                    </value>
                    <next>
                      <block type="variables_set" id=",k3e|97Q#zy~St|},FIw">
                        <field name="VAR" id="hKa[y{d-7SuUKfxML}Ib" variabletype="">RSI 2</field>
                        <value name="VALUE">
                          <block type="rsi" id="L`@9^C8dP8t_eY~kc`z@">
                            <value name="INPUT">
                              <block type="ohlc_values" id="!V~r6MSz?,gQ[8i%:iig">
                                <field name="OHLCFIELD_LIST">close</field>
                                <field name="CANDLEINTERVAL_LIST">default</field>
                              </block>
                            </value>
                            <value name="PERIOD">
                              <block type="math_number" id="M`iwUevPD`7AM;@a_lxL">
                                <field name="NUM">2</field>
                              </block>
                            </value>
                          </block>
                        </value>
                        <next>
                          <block type="notify" id="d6hoYghe$|5gGM!Uw4^E">
                            <field name="NOTIFICATION_TYPE">success</field>
                            <field name="NOTIFICATION_SOUND">silent</field>
                            <value name="MESSAGE">
                              <block type="text_join" id="0}QaY20UMMh`;6uUyJJV">
                                <mutation items="2"></mutation>
                                <value name="ADD0">
                                  <block type="text" id="rycoAM.71-1g2W0KNs9N">
                                    <field name="TEXT">RSI-CVC-2: </field>
                                  </block>
                                </value>
                                <value name="ADD1">
                                  <block type="variables_get" id="@6r^:%J(M%u/C:m.1,np">
                                    <field name="VAR" id="hKa[y{d-7SuUKfxML}Ib" variabletype="">RSI 2</field>
                                  </block>
                                </value>
                              </block>
                            </value>
                            <next>
                              <block type="variables_set" id="O=Rixb(-!$x4W_lcgCrs">
                                <field name="VAR" id="c,Ra=i;B*t9dXw#@K)lR" variabletype="">RSI</field>
                                <value name="VALUE">
                                  <block type="rsi" id="?K=mg]td}g~ceZ2fNmA7">
                                    <value name="INPUT">
                                      <block type="ticks" id="e_~L}YnK/hM,^s,0#.S_"></block>
                                    </value>
                                    <value name="PERIOD">
                                      <block type="math_number" id="/4CqJdIPSD,^ity}6T}O">
                                        <field name="NUM">14</field>
                                      </block>
                                    </value>
                                  </block>
                                </value>
                                <next>
                                  <block type="notify" id="]%/+4@.g_;SU83L[|g#F">
                                    <field name="NOTIFICATION_TYPE">success</field>
                                    <field name="NOTIFICATION_SOUND">silent</field>
                                    <value name="MESSAGE">
                                      <block type="text_join" id="a)u^d*Wv);[oYqk]MPry">
                                        <mutation items="2"></mutation>
                                        <value name="ADD0">
                                          <block type="text" id="Y)`6MSH*K=vm]W#y=)M^">
                                            <field name="TEXT">RSI14: </field>
                                          </block>
                                        </value>
                                        <value name="ADD1">
                                          <block type="variables_get" id="MuG~5Lk)=MX10qC:=ASZ">
                                            <field name="VAR" id="c,Ra=i;B*t9dXw#@K)lR" variabletype="">RSI</field>
                                          </block>
                                        </value>
                                      </block>
                                    </value>
                                    <next>
                                      <block type="controls_if" id="APyf7U`A;+:5P/cr@*ma">
                                        <value name="IF0">
                                          <block type="logic_operation" id="Fik@N=J6*Js,fFqeU[fa">
                                            <field name="OP">AND</field>
                                            <value name="A">
                                              <block type="logic_compare" id=";25)jh+O[!.ZgW0VF_{T">
                                                <field name="OP">GTE</field>
                                                <value name="A">
                                                  <block type="variables_get" id="HZnG$E+nU_6B%ljbBp]6">
                                                    <field name="VAR" id="hKa[y{d-7SuUKfxML}Ib" variabletype="">RSI 2</field>
                                                  </block>
                                                </value>
                                                <value name="B">
                                                  <block type="math_number" id="OfY!T]-(ah-4,L^Ps$sU">
                                                    <field name="NUM">90</field>
                                                  </block>
                                                </value>
                                              </block>
                                            </value>
                                            <value name="B">
                                              <block type="logic_compare" id="A6jp7O!Cn?Pd)3W:1Yu|">
                                                <field name="OP">GTE</field>
                                                <value name="A">
                                                  <block type="variables_get" id="7tBpRM6IguM%hyv+v++u">
                                                    <field name="VAR" id="c,Ra=i;B*t9dXw#@K)lR" variabletype="">RSI</field>
                                                  </block>
                                                </value>
                                                <value name="B">
                                                  <block type="math_number" id="$n{J6VDEaz?3}pA6,)%N">
                                                    <field name="NUM">65</field>
                                                  </block>
                                                </value>
                                              </block>
                                            </value>
                                          </block>
                                        </value>
                                        <statement name="DO0">
                                          <block type="purchase" id="P7KDue_%R`cnwH%87r@]">
                                            <field name="PURCHASE_LIST">PUT</field>
                                          </block>
                                        </statement>
                                        <next>
                                          <block type="controls_if" id="SprKx!v7j!AtOkEC?S/~">
                                            <value name="IF0">
                                              <block type="logic_operation" id=";Vi^JCyG.jwE,qGU^TTg">
                                                <field name="OP">AND</field>
                                                <value name="A">
                                                  <block type="logic_compare" id="+NBU5HydB-6L{p#k!7%*">
                                                    <field name="OP">LTE</field>
                                                    <value name="A">
                                                      <block type="variables_get" id="qR;s1EEvGxf6ybkhH1Y;">
                                                        <field name="VAR" id="hKa[y{d-7SuUKfxML}Ib" variabletype="">RSI 2</field>
                                                      </block>
                                                    </value>
                                                    <value name="B">
                                                      <block type="math_number" id="-PnBKV{w%|k0h}UAZTVo">
                                                        <field name="NUM">10</field>
                                                      </block>
                                                    </value>
                                                  </block>
                                                </value>
                                                <value name="B">
                                                  <block type="logic_compare" id="j@]y?cUcX5=|?:){tj9l">
                                                    <field name="OP">LTE</field>
                                                    <value name="A">
                                                      <block type="variables_get" id="HUMlay1(JhyPvw0]K26g">
                                                        <field name="VAR" id="c,Ra=i;B*t9dXw#@K)lR" variabletype="">RSI</field>
                                                      </block>
                                                    </value>
                                                    <value name="B">
                                                      <block type="math_number" id="@Szy#K?Pz.5SdEE`^*%v">
                                                        <field name="NUM">30</field>
                                                      </block>
                                                    </value>
                                                  </block>
                                                </value>
                                              </block>
                                            </value>
                                            <statement name="DO0">
                                              <block type="purchase" id="c|zWyU8VHh4#Lel;Z};=">
                                                <field name="PURCHASE_LIST">CALL</field>
                                              </block>
                                            </statement>
                                            <next>
                                              <block type="controls_if" id="FhOe,:{zPZJ`7aM)CI@[">
                                                <value name="IF0">
                                                  <block type="logic_operation" id="qWMAkd8nfYD$,Fci)x;]">
                                                    <field name="OP">AND</field>
                                                    <value name="A">
                                                      <block type="logic_compare" id="iO#{A#ig_Qwg#pdY?,s_">
                                                        <field name="OP">GTE</field>
                                                        <value name="A">
                                                          <block type="variables_get" id="./JCXx+I2F?A0.$;G,*t">
                                                            <field name="VAR" id="c,Ra=i;B*t9dXw#@K)lR" variabletype="">RSI</field>
                                                          </block>
                                                        </value>
                                                        <value name="B">
                                                          <block type="math_number" id="_P%RcdDIM0+*1|T6=H^m">
                                                            <field name="NUM">65</field>
                                                          </block>
                                                        </value>
                                                      </block>
                                                    </value>
                                                    <value name="B">
                                                      <block type="logic_operation" id="e:j#3dVLhg)*a*fl8L!_">
                                                        <field name="OP">AND</field>
                                                        <value name="A">
                                                          <block type="logic_compare" id="soaY`!8-=(_SgF[,9]9@">
                                                            <field name="OP">LT</field>
                                                            <value name="A">
                                                              <block type="variables_get" id="i_5lbFZKw4cFVQ(vaEfh">
                                                                <field name="VAR" id="mvV%E7GK^7Cx=BCxt/+N" variabletype="">spot4</field>
                                                              </block>
                                                            </value>
                                                            <value name="B">
                                                              <block type="variables_get" id="fSbfYsilAIWLvedLd!Wb">
                                                                <field name="VAR" id="V/`@i2l^h%BA/vg3V?Y_" variabletype="">spot3</field>
                                                              </block>
                                                            </value>
                                                          </block>
                                                        </value>
                                                        <value name="B">
                                                          <block type="logic_operation" id="]H.#QHt8u+23JqruVe`x">
                                                            <field name="OP">AND</field>
                                                            <value name="A">
                                                              <block type="logic_compare" id="nvI4tn4lOVqX|K_|F)Ar">
                                                                <field name="OP">LT</field>
                                                                <value name="A">
                                                                  <block type="variables_get" id="4u*]uXj+KqcObKQ{!!Q.">
                                                                    <field name="VAR" id="V/`@i2l^h%BA/vg3V?Y_" variabletype="">spot3</field>
                                                                  </block>
                                                                </value>
                                                                <value name="B">
                                                                  <block type="variables_get" id="PEe}z(cd=iK-|#Ak~rfv">
                                                                    <field name="VAR" id="R]}XJg8*ocRP#{pv/]hP" variabletype="">spot2</field>
                                                                  </block>
                                                                </value>
                                                              </block>
                                                            </value>
                                                            <value name="B">
                                                              <block type="logic_compare" id="s.1|wvsx[|@o5t;txn:Y">
                                                                <field name="OP">LT</field>
                                                                <value name="A">
                                                                  <block type="variables_get" id=",_W4Lew+pmC~cN(QRO]F">
                                                                    <field name="VAR" id="R]}XJg8*ocRP#{pv/]hP" variabletype="">spot2</field>
                                                                  </block>
                                                                </value>
                                                                <value name="B">
                                                                  <block type="variables_get" id="j!3pqJk#iD]JO=zA[^he">
                                                                    <field name="VAR" id="x{5)(}]`;Pr%_}EXY9BW" variabletype="">spot1</field>
                                                                  </block>
                                                                </value>
                                                              </block>
                                                            </value>
                                                          </block>
                                                        </value>
                                                      </block>
                                                    </value>
                                                  </block>
                                                </value>
                                                <statement name="DO0">
                                                  <block type="purchase" id="|.CzJ`9A.uUkRG6gpH=a">
                                                    <field name="PURCHASE_LIST">CALL</field>
                                                  </block>
                                                </statement>
                                                <next>
                                                  <block type="controls_if" id="z}2crZfZkm:Nr/zQdV=J">
                                                    <value name="IF0">
                                                      <block type="logic_operation" id="Rk72-U3@W/t)p;EQzE1+">
                                                        <field name="OP">AND</field>
                                                        <value name="A">
                                                          <block type="logic_compare" id="7dtP`D[1_RJZY6CGcJL@">
                                                            <field name="OP">LTE</field>
                                                            <value name="A">
                                                              <block type="variables_get" id="*W_gc@G58u}ra.3Q1a~.">
                                                                <field name="VAR" id="c,Ra=i;B*t9dXw#@K)lR" variabletype="">RSI</field>
                                                              </block>
                                                            </value>
                                                            <value name="B">
                                                              <block type="math_number" id="pCDt?#!t-+!FqKyk(}a,">
                                                                <field name="NUM">30</field>
                                                              </block>
                                                            </value>
                                                          </block>
                                                        </value>
                                                        <value name="B">
                                                          <block type="logic_operation" id="^d?pZ;x!E_JvG,C@Zq%/">
                                                            <field name="OP">AND</field>
                                                            <value name="A">
                                                              <block type="logic_compare" id="_3ikF@Eyl1bD6y)y,DPk">
                                                                <field name="OP">GT</field>
                                                                <value name="A">
                                                                  <block type="variables_get" id="CK(2}Rp#e$dnCWoC/t[B">
                                                                    <field name="VAR" id="mvV%E7GK^7Cx=BCxt/+N" variabletype="">spot4</field>
                                                                  </block>
                                                                </value>
                                                                <value name="B">
                                                                  <block type="variables_get" id="Ui^*_pc5CTFWzg/C!.M.">
                                                                    <field name="VAR" id="V/`@i2l^h%BA/vg3V?Y_" variabletype="">spot3</field>
                                                                  </block>
                                                                </value>
                                                              </block>
                                                            </value>
                                                            <value name="B">
                                                              <block type="logic_operation" id="Ld}dG[h-eD1]U#(ap{8k">
                                                                <field name="OP">AND</field>
                                                                <value name="A">
                                                                  <block type="logic_compare" id="B/_hJAlNi7$Qidi~Lr6j">
                                                                    <field name="OP">GT</field>
                                                                    <value name="A">
                                                                      <block type="variables_get" id=";fX6x$eal2E?T?dw}VtD">
                                                                        <field name="VAR" id="V/`@i2l^h%BA/vg3V?Y_" variabletype="">spot3</field>
                                                                      </block>
                                                                    </value>
                                                                    <value name="B">
                                                                      <block type="variables_get" id=":(t[zxsI]PF=et~2p%UQ">
                                                                        <field name="VAR" id="R]}XJg8*ocRP#{pv/]hP" variabletype="">spot2</field>
                                                                      </block>
                                                                    </value>
                                                                  </block>
                                                                </value>
                                                                <value name="B">
                                                                  <block type="logic_compare" id="TEkrR0zWLw%FdBK.(9sx">
                                                                    <field name="OP">GT</field>
                                                                    <value name="A">
                                                                      <block type="variables_get" id="F[ygF#47Q0tnGs`aEAcV">
                                                                        <field name="VAR" id="R]}XJg8*ocRP#{pv/]hP" variabletype="">spot2</field>
                                                                      </block>
                                                                    </value>
                                                                    <value name="B">
                                                                      <block type="variables_get" id="91+}$Nn0glvF_Mt!aezA">
                                                                        <field name="VAR" id="x{5)(}]`;Pr%_}EXY9BW" variabletype="">spot1</field>
                                                                      </block>
                                                                    </value>
                                                                  </block>
                                                                </value>
                                                              </block>
                                                            </value>
                                                          </block>
                                                        </value>
                                                      </block>
                                                    </value>
                                                    <statement name="DO0">
                                                      <block type="purchase" id="Go1LxE75PXX,$wZH}+^h">
                                                        <field name="PURCHASE_LIST">PUT</field>
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
  <block type="after_purchase" id="finish" x="-2" y="1202">
    <statement name="AFTERPURCHASE_STACK">
      <block type="controls_if" id="/TP%I,hfU)^|c.|/3ndN">
        <mutation else="1"></mutation>
        <value name="IF0">
          <block type="contract_check_result" id="!Ju)S0aU{UXQf0qHA6X,">
            <field name="CHECK_RESULT">win</field>
          </block>
        </value>
        <statement name="DO0">
          <block type="notify" id="gHD9SF(^C:~$q@c/;(KP">
            <field name="NOTIFICATION_TYPE">success</field>
            <field name="NOTIFICATION_SOUND">silent</field>
            <value name="MESSAGE">
              <block type="text_join" id="]Je7[};kvx`BRACG:?(;">
                <mutation items="2"></mutation>
                <value name="ADD0">
                  <block type="text" id="s/=(=W~@G6,IQ,b://B3">
                    <field name="TEXT">Won:</field>
                  </block>
                </value>
                <value name="ADD1">
                  <block type="read_details" id="SXm{k(Ltcd0rel3iez82">
                    <field name="DETAIL_INDEX">4</field>
                  </block>
                </value>
              </block>
            </value>
            <next>
              <block type="variables_set" id="!7vE(S.O$(Hp%A$z{Q)4">
                <field name="VAR" id="O~AXmG3`h:n`-WoDm)0~" variabletype="">Initial Amount</field>
                <value name="VALUE">
                  <block type="variables_get" id="xt{eOIX[E!rJ4}0f(|)w">
                    <field name="VAR" id="7iAq]Co?H(SF+qm5jgmD" variabletype="">Win Amount</field>
                  </block>
                </value>
              </block>
            </next>
          </block>
        </statement>
        <statement name="ELSE">
          <block type="notify" id="@^jo^p%_Dc9)/}ZVUN=q">
            <field name="NOTIFICATION_TYPE">warn</field>
            <field name="NOTIFICATION_SOUND">silent</field>
            <value name="MESSAGE">
              <block type="text_join" id="L!A5F7obJ6YDSU%sb~v$">
                <mutation items="2"></mutation>
                <value name="ADD0">
                  <block type="text" id=":bct,J@#aZ1,ap7%$u;m">
                    <field name="TEXT">Lost: </field>
                  </block>
                </value>
                <value name="ADD1">
                  <block type="math_single" id="Us=FXR=G20;r.vw#Qzx9">
                    <field name="OP">ABS</field>
                    <value name="NUM">
                      <shadow type="math_number" id="GleSn`9j7Cm7/dqg}FIA">
                        <field name="NUM">9</field>
                      </shadow>
                      <block type="read_details" id="6^U0{%K4N4+shx$i.^;H">
                        <field name="DETAIL_INDEX">4</field>
                      </block>
                    </value>
                  </block>
                </value>
              </block>
            </value>
            <next>
              <block type="math_change" id="Lp7Sf;6}.+aaQK7u|qC,">
                <field name="VAR" id="O~AXmG3`h:n`-WoDm)0~" variabletype="">Initial Amount</field>
                <value name="DELTA">
                  <shadow type="math_number" id="N=Vo^MVz~/^(xt7Ag@8E">
                    <field name="NUM">1</field>
                  </shadow>
                  <block type="math_arithmetic" id="eN7/Pe-C@6[cZuG=;sr|">
                    <field name="OP">MULTIPLY</field>
                    <value name="A">
                      <shadow type="math_number" id="ka8n8|Dugz,q5FkUjs`7">
                        <field name="NUM">1</field>
                      </shadow>
                      <block type="math_single" id="n#dZL(R~tbmwTs^YpY{n">
                        <field name="OP">ABS</field>
                        <value name="NUM">
                          <shadow type="math_number" id="GleSn`9j7Cm7/dqg}FIA">
                            <field name="NUM">9</field>
                          </shadow>
                          <block type="read_details" id="bV`6lc$_j`ElSi~fxG-e">
                            <field name="DETAIL_INDEX">4</field>
                          </block>
                        </value>
                      </block>
                    </value>
                    <value name="B">
                      <shadow type="math_number" id="{JXdZCp2%s=sfO@yN:n}">
                        <field name="NUM">1</field>
                      </shadow>
                      <block type="math_number" id="L2m6.74Wo}DL)X%A@uE}">
                        <field name="NUM">1.03</field>
                      </block>
                    </value>
                  </block>
                </value>
                <next>
                  <block type="controls_if" id="THEX=3SJ9vM.fn6isSQX">
                    <value name="IF0">
                      <block type="logic_compare" id=")?vQl#~,J(1mnfNi]c|F">
                        <field name="OP">GTE</field>
                        <value name="A">
                          <block type="math_single" id="AeT7xRW8;G`0dUU3G9Zu">
                            <field name="OP">ABS</field>
                            <value name="NUM">
                              <shadow type="math_number" id="ft^DVzOH^GlSjzUC}@3c">
                                <field name="NUM">9</field>
                              </shadow>
                              <block type="read_details" id="Dywmoc_eJ)3BDdpvZ+8%">
                                <field name="DETAIL_INDEX">4</field>
                              </block>
                            </value>
                          </block>
                        </value>
                        <value name="B">
                          <block type="variables_get" id="IR(@Z1;/dK1a7*)koIlK">
                            <field name="VAR" id="gy-(OQo2ivS$$4TQ+tcJ" variabletype="">Max Loss Amount</field>
                          </block>
                        </value>
                      </block>
                    </value>
                    <statement name="DO0">
                      <block type="text_print" id="MP:bns5WRrfs+]NCySeZ">
                        <value name="TEXT">
                          <shadow type="text" id="kqlrIk.GO.^}hI,PoUV)">
                            <field name="TEXT">abc</field>
                          </shadow>
                          <block type="text_join" id="l#77+N~6RSODKh?CeYY4">
                            <mutation items="2"></mutation>
                            <value name="ADD0">
                              <block type="text" id="+M,5;KZF~R7*zI2p0tec">
                                <field name="TEXT">Done! Total profit: </field>
                              </block>
                            </value>
                            <value name="ADD1">
                              <block type="total_profit" id="slBD+rxTQiUCbHHd6ka2"></block>
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
        <next>
          <block type="notify" id="1)tW7}^o?Ym2qm8-qmdO">
            <field name="NOTIFICATION_TYPE">info</field>
            <field name="NOTIFICATION_SOUND">silent</field>
            <value name="MESSAGE">
              <block type="text_join" id="t]P+(Nqhmu!Tg.F7-CPr">
                <mutation items="2"></mutation>
                <value name="ADD0">
                  <block type="text" id="7gm[}!($og`%Y,*D%j%;">
                    <field name="TEXT">Total Profit: </field>
                  </block>
                </value>
                <value name="ADD1">
                  <block type="total_profit" id="|K4ymCMY8D%B0Pqg?9ad"></block>
                </value>
              </block>
            </value>
            <next>
              <block type="controls_if" id="IuxXfH4y2;l}4;x^GXgv">
                <mutation else="1"></mutation>
                <value name="IF0">
                  <block type="logic_compare" id="Qq=J(YADm#qJRtdnM78y">
                    <field name="OP">LT</field>
                    <value name="A">
                      <block type="total_profit" id="W{-s|:=aTg]?pW@/|k~#"></block>
                    </value>
                    <value name="B">
                      <block type="variables_get" id="~h}JcSkFo$2+DvY7Z(i1">
                        <field name="VAR" id="$+4YB1~jnlepPV+/}y+j" variabletype="">Expected Profit</field>
                      </block>
                    </value>
                  </block>
                </value>
                <statement name="DO0">
                  <block type="trade_again" id=";?v.`3czHAz0=p.kKdO$"></block>
                </statement>
                <statement name="ELSE">
                  <block type="text_print" id="{#=T-jZoV^~Hg2fDop#P">
                    <value name="TEXT">
                      <shadow type="text" id="kqlrIk.GO.^}hI,PoUV)">
                        <field name="TEXT">abc</field>
                      </shadow>
                      <block type="text_join" id="LlYXC#rV|?[e@:Hp=,j=">
                        <mutation items="2"></mutation>
                        <value name="ADD0">
                          <block type="text" id="e{xh9Rs1RU:W_h6hSy/1">
                            <field name="TEXT">Done! Total profit: </field>
                          </block>
                        </value>
                        <value name="ADD1">
                          <block type="total_profit" id="TPWF3d]yS|:~*^VVyv]X"></block>
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
</xml>
