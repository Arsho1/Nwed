function noMoIb() {
    if (BLAZE.hecEjF) {
        BLAZE.hecEjF.MchKjg();
    };
    if (BLAZE.MJhjiB) {
        BLAZE.MJhjiB.MchKjg();
    };
    if (BLAZE.ofAPMm) {
        BLAZE.ofAPMm.MchKjg();
    };
    if (arguments[2] == 'unload') {
        return;
    };
    var faccjd;
    var FCIhjA = document.createElement('div');
    FCIhjA.id = 'BLAZE_Exit';
    document.body.appendChild(FCIhjA);
    if (arguments[2] == 'resource') {
        faccjd = GbiMej('exit_resource').replace('{URL}', 'javascript:BLAZE.global.gs.re()');
    } else if (arguments[2] == 'version') {
        faccjd = GbiMej('exit_version');
    } else if (arguments[2] == 'unique') {
        faccjd = GbiMej('exit_unique');
    } else {
        faccjd = GbiMej('exit_error') + '<br>' + arguments[2];
    };
    FCIhjA.innerHTML = faccjd;
};

function FggbgN() {
    if (BLAZE.ofAPMm) {
        if (BLAZE.PLATFORM == 'facebook') {
            BLAZE.ofAPMm.pKfbmj('auth.standby');
        } else {
            BLAZE.ofAPMm.pKfbmj('auth.entrance');
        }
    };
};

function LMFpLa() {
    if (BLAZE.GetENV('auth') == 1) {
        BLAZE.hecEjF.fkpbbL();
    } else {
        FggbgN();
    }
};
var peoHoE = (function () {
    var PMFAbI = BLAZE.GetENV('PROJECT_CONTENT_URL');
    var imMICB = {};
    imMICB.billiards = {};
    imMICB.billiards['gzpool'] = true;
    imMICB.billiards['straight'] = true;
    imMICB.billiards['8ball'] = true;
    imMICB.billiards['9ball'] = true;
    imMICB.billiards['snooker'] = true;
    imMICB.billiards['snookerplus'] = true;
    imMICB.billiards['pyramid'] = true;
    imMICB.billiards['scrpyramid'] = true;
    imMICB.billiards['carom'] = true;
    imMICB.billiards['onepocket'] = true;
    imMICB.billiards['anyeight'] = true;
    imMICB.billiards['bank'] = true;
    imMICB.billiards['combo'] = true;
    imMICB.billiards['scoreball'] = true;
    imMICB.chess = {
        gzchess: true
    };
    imMICB.checkers = {
        gzcheckers: true,
        amcheckers: true,
        anticheckers: true
    };
    var eAeFAO = {};
    eAeFAO.AelDEf = function () {
        if (NglBKa) {
            return null;
        };
        NglBKa = true;
        return HodpOF;
    };
    var NglBKa = false;
    var HodpOF = {};
    HodpOF.jdLpbp = function (bDLFNK, KPiBgE) {
        for (var nmLEoL in bDLFNK) {
            if (imMICB.hasOwnProperty(nmLEoL)) {
                var LJhpGD = bDLFNK[nmLEoL].split(':');
                var bmfhpd = LJhpGD.length;
                if (bmfhpd == 5) {
                    for (var fOGnCG = 0; fOGnCG < bmfhpd; fOGnCG++) {
                        LJhpGD[fOGnCG] = NmbiKM(LJhpGD[fOGnCG]);
                    };
                    KPiBgE[nmLEoL] = LJhpGD;
                }
            };
        }
    };
    HodpOF.ikmMBa = function (FJCela, bMjhAG) {
        var LJhpGD = FJCela.split(':');
        var bmfhpd = LJhpGD.length;
        if (bmfhpd == 5) {
            for (var fOGnCG = 0; fOGnCG < bmfhpd; fOGnCG++) {
                bMjhAG[fOGnCG] += NmbiKM(LJhpGD[fOGnCG]);
                if (bMjhAG[fOGnCG] < 0) {
                    bMjhAG[fOGnCG] = 0;
                }
            };
        }
    };
    HodpOF.ieMAIJ = function (bDLFNK, FeKiLh) {
        var OIkNGH = FeKiLh.stats_content.FeKiLh;
        var MAcnnN = [0, 0, 0, 0, 0];
        var hKbcfc = false;
        for (var nmLEoL in imMICB) {
            var HIjdLH = 'game_' + nmLEoL;
            if (bDLFNK.hasOwnProperty(nmLEoL)) {
                var HIhniL = bDLFNK[nmLEoL].split(':');
                if (HIhniL.length == 5) {
                    for (var fOGnCG = 0; fOGnCG < 5; fOGnCG++) {
                        HIhniL[fOGnCG] = NmbiKM(HIhniL[fOGnCG]);
                        MAcnnN[fOGnCG] += HIhniL[fOGnCG];
                    };
                    if (OIkNGH[HIjdLH] && HIhniL[2] > 0) {
                        OIkNGH[HIjdLH].style.display = '';
                        OIkNGH[nmLEoL + '_score'].innerHTML = HIhniL[0];
                        OIkNGH[nmLEoL + '_played'].innerHTML = HIhniL[2];
                        OIkNGH[nmLEoL + '_won'].innerHTML = HIhniL[3];
                        OIkNGH[nmLEoL + '_refused'].innerHTML = HIhniL[4];
                        hKbcfc = true;
                        continue;
                    }
                };
            };
            if (OIkNGH[HIjdLH]) {
                OIkNGH[HIjdLH].style.display = 'none';
            }
        };
        if (hKbcfc) {
            OIkNGH.no_stats.style.display = 'none';
        } else {
            OIkNGH.no_stats.style.display = '';
        };
        FeKiLh.score.innerHTML = GbiMej('user_overall_score').replace('[n]', '<b>' + HAELdp.OHokFB(MAcnnN[0] * 0.01) + '</b>');
        FeKiLh.ggvotes.innerHTML = GbiMej('user_overall_ggvotes').replace('[n]', '<b>' + MAcnnN[1] + '</b>');
    };
    HodpOF.NaCDop = function (bDLFNK, FeKiLh) {
        var OIkNGH = FeKiLh.stats_content.FeKiLh;
        var HaKCEN = false;
        var IDcDeC = 0;
        var HjjpMB = 0;
        for (var nmLEoL in imMICB) {
            var CpGPKn = OIkNGH['game_' + nmLEoL];
            if (bDLFNK.hasOwnProperty(nmLEoL)) {
                var LJhpGD = bDLFNK[nmLEoL];
                if (LJhpGD[2] > 0) {
                    HaKCEN = true;
                    IDcDeC += LJhpGD[0];
                    HjjpMB += LJhpGD[1];
                    CpGPKn.style.display = '';
                    OIkNGH[nmLEoL + '_score'].innerHTML = LJhpGD[0];
                    OIkNGH[nmLEoL + '_played'].innerHTML = LJhpGD[2];
                    OIkNGH[nmLEoL + '_won'].innerHTML = LJhpGD[3];
                    OIkNGH[nmLEoL + '_refused'].innerHTML = LJhpGD[4];
                    continue;
                }
            };
            CpGPKn.style.display = 'none';
        };
        if (!HaKCEN) {
            OIkNGH.no_stats.style.display = '';
        } else {
            OIkNGH.no_stats.style.display = 'none';
        };
        FeKiLh.score.innerHTML = GbiMej('user_overall_score').replace('[n]', '<b>' + HAELdp.OHokFB(IDcDeC * 0.01) + '</b>');
        FeKiLh.ggvotes.innerHTML = GbiMej('user_overall_ggvotes').replace('[n]', '<b>' + HjjpMB + '</b>');
    };
    HodpOF.gGGnFL = function (fhEmFp) {
        if (!fhEmFp) {
            return;
        };
        var FeKiLh = fhEmFp.FeKiLh;
        for (var HaIMJf in imMICB) {
            var oAIJEo = FeKiLh[HaIMJf + '_type'];
            var cFbLpo = 'game_' + HaIMJf + '_';
            if (oAIJEo) {
                var InIPKb = imMICB[HaIMJf];
                for (var cfNBgC in InIPKb) {
                    var HDDJiB = document.createElement('option');
                    HDDJiB.value = cfNBgC;
                    HDDJiB.innerHTML = GbiMej(cFbLpo + cfNBgC);
                    oAIJEo.appendChild(HDDJiB);
                }
            };
        }
    };
    HodpOF.BBjgfc = function (pmGLhe) {
        if (!pmGLhe) {
            return;
        };
        var FeKiLh = pmGLhe.FeKiLh;
        for (var HaIMJf in imMICB) {
            var oAIJEo = FeKiLh[HaIMJf + '_start_type'];
            var cFbLpo = 'game_' + HaIMJf + '_';
            if (oAIJEo) {
                var InIPKb = imMICB[HaIMJf];
                for (var cfNBgC in InIPKb) {
                    var HDDJiB = document.createElement('option');
                    HDDJiB.value = cfNBgC;
                    HDDJiB.innerHTML = GbiMej(cFbLpo + cfNBgC);
                    oAIJEo.appendChild(HDDJiB);
                }
            };
        }
    };
    HodpOF.EOmmPk = function (oAIJEo, dfKgdP) {
        dfKgdP = String(dfKgdP);
        if (oAIJEo.KioofC === dfKgdP) {
            return;
        };
        oAIJEo.KioofC = dfKgdP;
        ggGkJc.BKMJhm(oAIJEo);
        var mJeAlE;
        if (dfKgdP != '') {
            if (!imMICB.hasOwnProperty(dfKgdP)) {
                return;
            };
            mJeAlE = [dfKgdP];
        } else {
            mJeAlE = Object.keys(imMICB);
        };
        var HDDJiB, CCAldd, cFbLpo, InIPKb, bmfhpd = mJeAlE.length;
        for (var fOGnCG = 0; fOGnCG < bmfhpd; fOGnCG++) {
            var HaIMJf = mJeAlE[fOGnCG];
            CCAldd = HaIMJf + ':';
            cFbLpo = 'game_' + HaIMJf + '_';
            HDDJiB = document.createElement('option');
            HDDJiB.className = 'game_title';
            HDDJiB.value = CCAldd;
            HDDJiB.innerHTML = GbiMej('game_' + HaIMJf);
            oAIJEo.appendChild(HDDJiB);
            InIPKb = imMICB[HaIMJf];
            for (var cfNBgC in InIPKb) {
                HDDJiB = document.createElement('option');
                HDDJiB.value = CCAldd + cfNBgC;
                HDDJiB.innerHTML = GbiMej(cFbLpo + cfNBgC);
                oAIJEo.appendChild(HDDJiB);
            }
        };
    };
    HodpOF.JApbeK = function (nOjnHj, MlomAd) {
        var MlomAd = String(MlomAd).split('$');
        var fMnbiD, DILNMg, fOGnCG, bmfhpd = MlomAd.length;
        if (bmfhpd < 2) {
            return null;
        };
        var kBkBEC = {};
        kBkBEC.nOjnHj = String(nOjnHj);
        kBkBEC.ECEngc = NmbiKM(MlomAd.shift());
        kBkBEC.MplMCo = [];
        bmfhpd--;
        for (fOGnCG = 0; fOGnCG < bmfhpd; fOGnCG++) {
            DILNMg = MlomAd[fOGnCG].split('^');
            if (DILNMg.length == 3) {
                kBkBEC.HBNKDb = DILNMg.shift();
            };
            if (DILNMg.length != 2) {
                return null;
            };
            fMnbiD = {};
            if (DILNMg[0] != '') {
                fMnbiD.gv = DILNMg[0];
            };
            if (DILNMg[1] != '') {
                fMnbiD.gs = DILNMg[1];
            };
            kBkBEC.MplMCo.push(fMnbiD);
        };
        if (kBkBEC.HBNKDb === undefined) {
            return null;
        };
        return kBkBEC;
    };
    var aPMNpJ = '';
    var CGbapk = null;
    var eInbpO = [0, 0];
    var cghbDa = [10, 10];
    var mFDlLh = [10, 10];
    var oOOlDn = {};
    var KodbFi = {};
    HodpOF.pPGDDg = function (InepGi) {
        if (aPMNpJ == '') {
            return null;
        };
        if (!oOOlDn) {
            return null;
        };
        if (CGbapk) {
            var ipgFmB = CGbapk.FeKiLh.GSP_Preview;
            window.removeEventListener('resize', kEjJEM, false);
            ipgFmB.removeEventListener('mousemove', dGpcdK, false);
            ipgFmB.removeEventListener('touchstart', kDGalH, false);
            ipgFmB.removeEventListener('touchmove', kDGalH, false);
        };
        aPMNpJ = '';
        var NoHpOe = null;
        for (var EchcgD in oOOlDn) {
            var hflkkN = false;
            var NAlaeO = oOOlDn[EchcgD].JBLcPD;
            var mNiFLg = oOOlDn[EchcgD].pGiAAe;
            for (var hJBOIC in NAlaeO) {
                if (NAlaeO[hJBOIC] != mNiFLg[hJBOIC]) {
                    hflkkN = true;
                    break;
                }
            };
            if (hflkkN) {
                var PdljhP = null;
                if (EchcgD == 'billiards') {
                    var dchiKB = mNiFLg.dchiKB;
                    if (dchiKB < 100) {
                        dchiKB = 0;
                    };
                    PdljhP = {
                        c: dchiKB,
                        f: mNiFLg.nOHEMd,
                        t: mNiFLg.eaGHGh,
                        b: mNiFLg.hHlnBA,
                        e: mNiFLg.LIHMme
                    };
                } else if (EchcgD == 'chess') {
                    PdljhP = {
                        b: mNiFLg.LHjjbf,
                        f: mNiFLg.lfkIiA,
                        e: mNiFLg.LIHMme
                    };
                } else if (EchcgD == 'checkers') {
                    PdljhP = {
                        b: mNiFLg.LHjjbf,
                        f: mNiFLg.lfkIiA,
                        e: mNiFLg.LIHMme
                    };
                } else {
                    continue;
                };
                if (PdljhP) {
                    InepGi.kojJNb.options[EchcgD] = PdljhP;
                    if (!NoHpOe) {
                        NoHpOe = {};
                    };
                    NoHpOe[EchcgD] = PdljhP;
                }
            };
        };
        return NoHpOe;
    };
    HodpOF.hkeaOf = function (InepGi, fFOAfi, JpgfHB) {
        aPMNpJ = fFOAfi;
        CGbapk = JpgfHB;
        if (!oOOlDn[aPMNpJ]) {
            oOOlDn[aPMNpJ] = {
                diOAaj: 0,
                JBLcPD: {},
                pGiAAe: {},
                GNHHhP: {},
                NCFKjC: {}
            };
        };
        var FeKiLh = CGbapk.FeKiLh;
        var NAlaeO = oOOlDn[aPMNpJ].JBLcPD;
        var mNiFLg = oOOlDn[aPMNpJ].pGiAAe;
        if (InepGi.kojJNb.statistics[aPMNpJ]) {
            oOOlDn[aPMNpJ].diOAaj = NmbiKM(InepGi.kojJNb.statistics[aPMNpJ][0]);
        } else {
            oOOlDn[aPMNpJ].diOAaj = 0;
        };
        var NJLHgo = InepGi.cmNcCD.w;
        var bHLMFD = BLAZE.gbgcbP;
        var kAoHDI = Object.keys(NJLHgo);
        var aagdAI = kAoHDI.length;
        var eGNnCD = CbPkDM(oOOlDn[aPMNpJ].diOAaj);
        var iIakJG, LfEFlm, oeigjE, DILNMg, fOGnCG, OKIOal, HDDJiB;
        var DpBkDG, GpjlGC = InepGi.kojJNb.options[aPMNpJ];
        var EKlGkf = BLAZE.CONTENT_VERSION;
        if (aPMNpJ == 'billiards') {
            FeKiLh.gst_billiards_table_select.onchange = bHmkNb;
            FeKiLh.gst_billiards_bg_select.onchange = fmmGjc;
            FeKiLh.gst_billiards_effect_select.onchange = IoMcJN;
            var ipgFmB = CGbapk.FeKiLh.GSP_Preview;
            window.addEventListener('resize', kEjJEM, false);
            ipgFmB.addEventListener('mousemove', dGpcdK, false);
            ipgFmB.addEventListener('touchstart', kDGalH, false);
            ipgFmB.addEventListener('touchmove', kDGalH, false);
            OKIOal = kAoHDI.join(':') + eGNnCD;
            if (KodbFi[aPMNpJ] !== OKIOal) {
                KodbFi[aPMNpJ] = OKIOal;
                FeKiLh.gst_billiards_cue_select.onchange = EpBGec;
                ggGkJc.BKMJhm(FeKiLh.gst_billiards_cue_select);
                HDDJiB = document.createElement('option');
                HDDJiB.value = 0;
                HDDJiB.innerHTML = GbiMej('standard_item');
                FeKiLh.gst_billiards_cue_select.appendChild(HDDJiB);
                FeKiLh.gst_billiards_table_select.onchange = bHmkNb;
                ggGkJc.BKMJhm(FeKiLh.gst_billiards_table_select);
                HDDJiB = document.createElement('option');
                HDDJiB.value = 0;
                HDDJiB.innerHTML = GbiMej('standard_item');
                FeKiLh.gst_billiards_table_select.appendChild(HDDJiB);
                FeKiLh.gst_billiards_bg_select.onchange = fmmGjc;
                ggGkJc.BKMJhm(FeKiLh.gst_billiards_bg_select);
                HDDJiB = document.createElement('option');
                HDDJiB.value = 0;
                HDDJiB.innerHTML = GbiMej('no_background');
                FeKiLh.gst_billiards_bg_select.appendChild(HDDJiB);
                FeKiLh.gst_billiards_effect_select.onchange = IoMcJN;
                ggGkJc.BKMJhm(FeKiLh.gst_billiards_effect_select);
                HDDJiB = document.createElement('option');
                HDDJiB.value = 0;
                HDDJiB.innerHTML = GbiMej('no_effect');
                FeKiLh.gst_billiards_effect_select.appendChild(HDDJiB);
                ggGkJc.BKMJhm(FeKiLh.fabric_set);
                HDDJiB = document.createElement('div');
                HDDJiB.eDpcMa = 0;
                HDDJiB.className = 'FabricSlot';
                HDDJiB.style.backgroundImage = 'url("' + BLAZE.nhjLnH.oAclpm('bitmap', 'billiards_default_fabric').src + '")';
                hOFFNd.foifJe(HDDJiB, JfFJij, [0], false);
                FeKiLh.fabric_set.appendChild(HDDJiB);
                for (iIakJG = 0; iIakJG < aagdAI; iIakJG++) {
                    DILNMg = kAoHDI[iIakJG];
                    if (!bHLMFD.hasOwnProperty(DILNMg)) {
                        continue;
                    };
                    if (bHLMFD[DILNMg].length > 1) {
                        if (bHLMFD[DILNMg][1] !== 'gamezer') {
                            continue;
                        }
                    };
                    if (DILNMg.substr(0, 4) == 'pcue') {
                        DILNMg = NmbiKM(DILNMg.substr(4));
                        HDDJiB = document.createElement('option');
                        HDDJiB.value = DILNMg + 100;
                        HDDJiB.innerHTML = GbiMej('inv_pcue' + DILNMg);
                        FeKiLh.gst_billiards_cue_select.appendChild(HDDJiB);
                    } else if (DILNMg.substr(0, 4) == 'acue') {
                        DILNMg = NmbiKM(DILNMg.substr(4));
                        HDDJiB = document.createElement('option');
                        HDDJiB.value = DILNMg + 1000;
                        HDDJiB.innerHTML = GbiMej('inv_acue' + DILNMg);
                        FeKiLh.gst_billiards_cue_select.appendChild(HDDJiB);
                    } else if (DILNMg.substr(0, 3) == 'ttb') {
                        DILNMg = NmbiKM(DILNMg.substr(3));
                        HDDJiB = document.createElement('option');
                        HDDJiB.value = DILNMg;
                        HDDJiB.innerHTML = GbiMej('inv_ttb' + DILNMg);
                        FeKiLh.gst_billiards_table_select.appendChild(HDDJiB);
                    } else if (DILNMg.substr(0, 3) == 'tbg') {
                        DILNMg = NmbiKM(DILNMg.substr(3));
                        HDDJiB = document.createElement('option');
                        HDDJiB.value = DILNMg;
                        HDDJiB.innerHTML = GbiMej('inv_tbg' + DILNMg);
                        FeKiLh.gst_billiards_bg_select.appendChild(HDDJiB);
                    } else if (DILNMg.substr(0, 2) == 'be') {
                        DILNMg = NmbiKM(DILNMg.substr(2));
                        HDDJiB = document.createElement('option');
                        HDDJiB.value = DILNMg;
                        HDDJiB.innerHTML = GbiMej('inv_be' + DILNMg);
                        FeKiLh.gst_billiards_effect_select.appendChild(HDDJiB);
                    } else if (DILNMg.substr(0, 3) == 'fbr') {
                        DILNMg = NmbiKM(DILNMg.substr(3));
                        if (DILNMg == 0) {
                            fOGnCG = 1;
                        } else {
                            fOGnCG = 0;
                        };
                        DILNMg = DILNMg * 100;
                        for (LfEFlm = fOGnCG; LfEFlm < 5; LfEFlm++) {
                            oeigjE = DILNMg + LfEFlm;
                            HDDJiB = document.createElement('div');
                            HDDJiB.eDpcMa = oeigjE;
                            HDDJiB.className = 'FabricSlot';
                            HDDJiB.style.backgroundImage = 'url("' + PMFAbI + 'fbr' + oeigjE + '.png?' + EKlGkf + '")';
                            hOFFNd.foifJe(HDDJiB, JfFJij, [oeigjE], false);
                            FeKiLh.fabric_set.appendChild(HDDJiB);
                        }
                    };
                };
                HDDJiB = document.createElement('div');
                HDDJiB.className = 'clear';
                FeKiLh.fabric_set.appendChild(HDDJiB);
            };
            mNiFLg.dchiKB = eGNnCD;
            if (GpjlGC.c > 1000) {
                DpBkDG = 'acue' + (GpjlGC.c - 1000);
                if (NJLHgo.hasOwnProperty(DpBkDG) && bHLMFD.hasOwnProperty(DpBkDG)) {
                    mNiFLg.dchiKB = GpjlGC.c;
                }
            } else if (GpjlGC.c > 100) {
                DpBkDG = 'pcue' + (GpjlGC.c - 100);
                if (NJLHgo.hasOwnProperty(DpBkDG) && bHLMFD.hasOwnProperty(DpBkDG)) {
                    mNiFLg.dchiKB = GpjlGC.c;
                }
            };
            NAlaeO.dchiKB = mNiFLg.dchiKB;
            if (mNiFLg.dchiKB < 100) {
                FeKiLh.gst_billiards_cue_select.value = 0;
            } else {
                FeKiLh.gst_billiards_cue_select.value = mNiFLg.dchiKB;
            };
            mNiFLg.LIHMme = 0;
            mNiFLg.eaGHGh = 0;
            if (GpjlGC.t > 0) {
                DpBkDG = 'ttb' + GpjlGC.t;
                if (NJLHgo.hasOwnProperty(DpBkDG) && bHLMFD.hasOwnProperty(DpBkDG)) {
                    mNiFLg.eaGHGh = GpjlGC.t;
                }
            };
            NAlaeO.eaGHGh = mNiFLg.eaGHGh;
            FeKiLh.gst_billiards_table_select.value = mNiFLg.eaGHGh;
            mNiFLg.nOHEMd = 0;
            if (GpjlGC.f > 0) {
                var DFPJlG = GpjlGC.f % 100;
                var ifBmKh = (GpjlGC.f - DFPJlG) * 0.01;
                DpBkDG = 'fbr' + ifBmKh;
                if (NJLHgo.hasOwnProperty(DpBkDG) && bHLMFD.hasOwnProperty(DpBkDG)) {
                    if (DFPJlG > 4) {
                        DFPJlG = 4;
                    };
                    mNiFLg.nOHEMd = (ifBmKh * 100) + DFPJlG;
                }
            };
            NAlaeO.nOHEMd = mNiFLg.nOHEMd;
            mNiFLg.hHlnBA = 0;
            if (GpjlGC.b > 0) {
                DpBkDG = 'tbg' + GpjlGC.b;
                if (NJLHgo.hasOwnProperty(DpBkDG) && bHLMFD.hasOwnProperty(DpBkDG)) {
                    mNiFLg.hHlnBA = GpjlGC.b;
                }
            };
            NAlaeO.hHlnBA = mNiFLg.hHlnBA;
            FeKiLh.gst_billiards_bg_select.value = mNiFLg.hHlnBA;
            mNiFLg.LIHMme = 0;
            if (GpjlGC.e > 0) {
                DpBkDG = 'be' + GpjlGC.e;
                if (NJLHgo.hasOwnProperty(DpBkDG) && bHLMFD.hasOwnProperty(DpBkDG)) {
                    mNiFLg.LIHMme = GpjlGC.e;
                }
            };
            NAlaeO.LIHMme = mNiFLg.LIHMme;
            FeKiLh.gst_billiards_effect_select.value = mNiFLg.LIHMme;
            kEjJEM();
            JfFJij(NAlaeO.nOHEMd)
        } else if (aPMNpJ == 'chess') {
            FeKiLh.gst_chess_board_select.onchange = ogIOfD;
            ggGkJc.BKMJhm(FeKiLh.gst_chess_board_select);
            HDDJiB = document.createElement('option');
            HDDJiB.value = 0;
            HDDJiB.innerHTML = GbiMej('standard_item');
            FeKiLh.gst_chess_board_select.appendChild(HDDJiB);
            for (iIakJG = 0; iIakJG < aagdAI; iIakJG++) {
                DILNMg = kAoHDI[iIakJG];
                if (!bHLMFD.hasOwnProperty(DILNMg)) {
                    continue;
                };
                if (bHLMFD[DILNMg].length > 1) {
                    if (bHLMFD[DILNMg][1] !== 'gamezer') {
                        continue;
                    }
                };
                if (DILNMg.substr(0, 3) == 'chb') {
                    DILNMg = NmbiKM(DILNMg.substr(3));
                    HDDJiB = document.createElement('option');
                    HDDJiB.value = DILNMg;
                    HDDJiB.innerHTML = GbiMej('inv_chb' + DILNMg);
                    FeKiLh.gst_chess_board_select.appendChild(HDDJiB);
                } else if (DILNMg.substr(0, 3) == 'csf') {
                    DILNMg = NmbiKM(DILNMg.substr(3));
                    HDDJiB = document.createElement('option');
                    HDDJiB.value = DILNMg;
                    HDDJiB.innerHTML = GbiMej('inv_csf' + DILNMg);
                    FeKiLh.gst_chess_pieceset_select.appendChild(HDDJiB);
                }
            };
            mNiFLg.LHjjbf = 0;
            if (GpjlGC.b > 0) {
                DpBkDG = 'chb' + GpjlGC.b;
                if (NJLHgo.hasOwnProperty(DpBkDG) && bHLMFD.hasOwnProperty(DpBkDG)) {
                    mNiFLg.LHjjbf = GpjlGC.b;
                }
            };
            NAlaeO.LHjjbf = mNiFLg.LHjjbf;
            FeKiLh.gst_chess_board_select.value = mNiFLg.LHjjbf;
            mNiFLg.LIHMme = 0;
            oaAmdc();
        } else if (aPMNpJ == 'checkers') {
            FeKiLh.gst_checkers_board_select.onchange = OcappP;
            ggGkJc.BKMJhm(FeKiLh.gst_checkers_board_select);
            HDDJiB = document.createElement('option');
            HDDJiB.value = 0;
            HDDJiB.innerHTML = GbiMej('standard_item');
            FeKiLh.gst_checkers_board_select.appendChild(HDDJiB);
            FeKiLh.gst_checkers_pieceset_select.onchange = flBkdb;
            ggGkJc.BKMJhm(FeKiLh.gst_checkers_pieceset_select);
            HDDJiB = document.createElement('option');
            HDDJiB.value = 0;
            HDDJiB.innerHTML = GbiMej('standard_item');
            FeKiLh.gst_checkers_pieceset_select.appendChild(HDDJiB);
            for (iIakJG = 0; iIakJG < aagdAI; iIakJG++) {
                DILNMg = kAoHDI[iIakJG];
                if (!bHLMFD.hasOwnProperty(DILNMg)) {
                    continue;
                };
                if (bHLMFD[DILNMg].length > 1) {
                    if (bHLMFD[DILNMg][1] !== 'gamezer') {
                        continue;
                    }
                };
                if (DILNMg.substr(0, 3) == 'chb') {
                    DILNMg = NmbiKM(DILNMg.substr(3));
                    HDDJiB = document.createElement('option');
                    HDDJiB.value = DILNMg;
                    HDDJiB.innerHTML = GbiMej('inv_chb' + DILNMg);
                    FeKiLh.gst_checkers_board_select.appendChild(HDDJiB);
                } else if (DILNMg.substr(0, 3) == 'ckf') {
                    DILNMg = NmbiKM(DILNMg.substr(3));
                    HDDJiB = document.createElement('option');
                    HDDJiB.value = DILNMg;
                    HDDJiB.innerHTML = GbiMej('inv_ckf' + DILNMg);
                    FeKiLh.gst_checkers_pieceset_select.appendChild(HDDJiB);
                }
            };
            mNiFLg.LHjjbf = 0;
            if (GpjlGC.b > 0) {
                DpBkDG = 'chb' + GpjlGC.b;
                if (NJLHgo.hasOwnProperty(DpBkDG) && bHLMFD.hasOwnProperty(DpBkDG)) {
                    mNiFLg.LHjjbf = GpjlGC.b;
                }
            };
            NAlaeO.LHjjbf = mNiFLg.LHjjbf;
            FeKiLh.gst_checkers_board_select.value = mNiFLg.LHjjbf;
            mNiFLg.lfkIiA = 0;
            if (GpjlGC.f > 0) {
                DpBkDG = 'ckf' + GpjlGC.f;
                if (NJLHgo.hasOwnProperty(DpBkDG) && bHLMFD.hasOwnProperty(DpBkDG)) {
                    mNiFLg.lfkIiA = GpjlGC.f;
                }
            };
            NAlaeO.lfkIiA = mNiFLg.lfkIiA;
            FeKiLh.gst_checkers_pieceset_select.value = mNiFLg.lfkIiA;
            mNiFLg.LIHMme = 0;
            oaAmdc();
        }
    };

    function oaAmdc() {
        if (aPMNpJ == '') {
            return;
        };
        if (!CGbapk) {
            return;
        };
        if (!oOOlDn[aPMNpJ]) {
            return;
        };
        var FeKiLh = CGbapk.FeKiLh;
        var mNiFLg = oOOlDn[aPMNpJ].pGiAAe;
        var KPjhkP = oOOlDn[aPMNpJ].GNHHhP;
        var BGcfbl = oOOlDn[aPMNpJ].NCFKjC;
        var pKaopF;
        if (aPMNpJ == 'billiards') {
            if (mNiFLg.dchiKB !== KPjhkP.dchiKB) {
                pKaopF = mNiFLg.dchiKB;
                KPjhkP.dchiKB = pKaopF;
                if (pKaopF < 100) {
                    if (pKaopF < 1) {
                        FeKiLh.GSP_Cue.style.backgroundImage = 'url("' + BLAZE.nhjLnH.oAclpm('bitmap', 'billiards_default_cue').src + '")';
                    } else {
                        CGbapk.classList.add('loadgsc');
                        BGcfbl.dchiKB = true;
                        pKaopF = 'cue' + pKaopF;
                        BLAZE.nhjLnH.dkgJMA(pKaopF, PMFAbI + pKaopF + '.png?' + BLAZE.CONTENT_VERSION, 1, DGpDkg, 'dchiKB');
                    }
                } else if (pKaopF < 1000) {
                    pKaopF -= 100;
                    CGbapk.classList.add('loadgsc');
                    BGcfbl.dchiKB = true;
                    pKaopF = 'pcue' + pKaopF;
                    BLAZE.nhjLnH.dkgJMA(pKaopF, PMFAbI + pKaopF + '.png?' + BLAZE.CONTENT_VERSION, 1, DGpDkg, 'dchiKB');
                } else {
                    pKaopF -= 1000;
                    CGbapk.classList.add('loadgsc');
                    BGcfbl.dchiKB = true;
                    pKaopF = 'apcue' + pKaopF;
                    BLAZE.nhjLnH.dkgJMA(pKaopF, PMFAbI + pKaopF + '.png?' + BLAZE.CONTENT_VERSION, 1, DGpDkg, 'dchiKB');
                }
            };
            if (mNiFLg.eaGHGh !== KPjhkP.eaGHGh) {
                pKaopF = mNiFLg.eaGHGh;
                KPjhkP.eaGHGh = pKaopF;
                if (pKaopF == 0) {
                    FeKiLh.GSP_Table.style.backgroundImage = 'url("' + BLAZE.nhjLnH.oAclpm('bitmap', 'billiards_default_table').src + '")';
                } else {
                    CGbapk.classList.add('loadgsc');
                    BGcfbl.eaGHGh = true;
                    pKaopF = 'ttb' + pKaopF;
                    BLAZE.nhjLnH.dkgJMA(pKaopF, PMFAbI + pKaopF + '.png?' + BLAZE.CONTENT_VERSION, 1, DGpDkg, 'eaGHGh');
                }
            };
            if (mNiFLg.nOHEMd !== KPjhkP.nOHEMd) {
                pKaopF = mNiFLg.nOHEMd;
                KPjhkP.nOHEMd = pKaopF;
                if (pKaopF == 0) {
                    FeKiLh.GSP_Fabric.style.backgroundImage = 'url("' + BLAZE.nhjLnH.oAclpm('bitmap', 'billiards_default_fabric').src + '")';
                } else {
                    CGbapk.classList.add('loadgsc');
                    BGcfbl.nOHEMd = true;
                    pKaopF = 'fbr' + pKaopF;
                    BLAZE.nhjLnH.dkgJMA(pKaopF, PMFAbI + pKaopF + '.png?' + BLAZE.CONTENT_VERSION, 1, DGpDkg, 'nOHEMd');
                }
            };
            if (mNiFLg.hHlnBA !== KPjhkP.hHlnBA) {
                KPjhkP.hHlnBA = mNiFLg.hHlnBA;
            }
        } else if (aPMNpJ == 'chess') {} else if (aPMNpJ == 'checkers') {}
    };

    function DGpDkg(BiAKPf, aCKfgg, dFlGoB) {
        if (!aCKfgg) {
            return;
        };
        if (aPMNpJ == '') {
            return;
        };
        if (!CGbapk) {
            return;
        };
        if (!oOOlDn[aPMNpJ]) {
            return;
        };
        var KPjhkP = oOOlDn[aPMNpJ].GNHHhP;
        var BGcfbl = oOOlDn[aPMNpJ].NCFKjC;
        var FeKiLh = CGbapk.FeKiLh;
        if (dFlGoB == 'dchiKB') {
            if (KPjhkP.dchiKB != 0) {
                BGcfbl[dFlGoB] = false;
                FeKiLh.GSP_Cue.style.backgroundImage = 'url("' + aCKfgg.src + '")';
            }
        } else if (dFlGoB == 'eaGHGh') {
            if (KPjhkP.eaGHGh != 0) {
                BGcfbl[dFlGoB] = false;
                FeKiLh.GSP_Table.style.backgroundImage = 'url("' + aCKfgg.src + '")';
            }
        } else if (dFlGoB == 'nOHEMd') {
            if (KPjhkP.nOHEMd != 0) {
                BGcfbl[dFlGoB] = false;
                FeKiLh.GSP_Fabric.style.backgroundImage = 'url("' + aCKfgg.src + '")';
            }
        } else {
            $warn(61190395);
            return;
        };
        for (var hJBOIC in BGcfbl) {
            if (BGcfbl[hJBOIC]) {
                return;
            }
        };
        CGbapk.classList.remove('loadgsc');
    };

    function FHkfff(dfgHKn) {
        if (aPMNpJ == '') {
            return;
        };
        if (!CGbapk) {
            return;
        };
        var FeKiLh = CGbapk.FeKiLh;
        lJELmO.IFDeod(dfgHKn, eInbpO);
        var ipgFmB = CGbapk.FeKiLh.GSP_CueContanier;
        var PPkOnP = dfgHKn[0] / cghbDa[0];
        if (PPkOnP < 0) {
            PPkOnP = 0;
        } else if (PPkOnP > 1) {
            PPkOnP = 1;
        };
        FeKiLh.GSP_CueContanier.style.left = (390 + HAELdp.BObpdE(-PPkOnP * (70 + mFDlLh[1] - cghbDa[0]))) + 'px'
    };

    function dGpcdK(EAmjJJ) {
        FHkfff([EAmjJJ.clientX, EAmjJJ.clientY]);
    };

    function kDGalH(EAmjJJ) {
        if (EAmjJJ.changedTouches.length < 1) {
            return;
        };
        var lboAhk = EAmjJJ.changedTouches[0];
        FHkfff([lboAhk.clientX, lboAhk.clientY]);
    };

    function kEjJEM(EAmjJJ) {
        if (aPMNpJ == '') {
            return;
        };
        if (!CGbapk) {
            return;
        };
        var FeKiLh = CGbapk.FeKiLh;
        eInbpO = ggGkJc.oAcDfp(FeKiLh.GSP_Preview);
        eInbpO[0] -= FeKiLh.switcher.offsetWidth * 0.25;
        cghbDa[0] = FeKiLh.GSP_Preview.offsetWidth;
        cghbDa[1] = FeKiLh.GSP_Preview.offsetHeight;
        mFDlLh[0] = FeKiLh.GSP_CueContanier.offsetWidth;
        mFDlLh[1] = FeKiLh.GSP_CueContanier.offsetHeight;
        FHkfff([0, 0]);
    };

    function EpBGec() {
        if (aPMNpJ == '') {
            return;
        };
        if (!CGbapk) {
            return;
        };
        if (!CGbapk.parentNode) {
            return;
        };
        if (!oOOlDn[aPMNpJ]) {
            return;
        };
        oOOlDn[aPMNpJ].pGiAAe.dchiKB = NmbiKM(CGbapk.FeKiLh.gst_billiards_cue_select.value);
        oaAmdc();
    };

    function bHmkNb() {
        if (aPMNpJ == '') {
            return;
        };
        if (!CGbapk) {
            return;
        };
        if (!CGbapk.parentNode) {
            return;
        };
        if (!oOOlDn[aPMNpJ]) {
            return;
        };
        oOOlDn[aPMNpJ].pGiAAe.eaGHGh = NmbiKM(CGbapk.FeKiLh.gst_billiards_table_select.value);
        oaAmdc();
    };

    function flBkdb() {
        if (aPMNpJ == '') {
            return;
        };
        if (!CGbapk) {
            return;
        };
        if (!CGbapk.parentNode) {
            return;
        };
        if (!oOOlDn[aPMNpJ]) {
            return;
        };
        oOOlDn[aPMNpJ].pGiAAe.lfkIiA = NmbiKM(CGbapk.FeKiLh.gst_checkers_pieceset_select.value);
        oaAmdc();
    };

    function ogIOfD() {
        if (aPMNpJ == '') {
            return;
        };
        if (!CGbapk) {
            return;
        };
        if (!CGbapk.parentNode) {
            return;
        };
        if (!oOOlDn[aPMNpJ]) {
            return;
        };
        oOOlDn[aPMNpJ].pGiAAe.LHjjbf = NmbiKM(CGbapk.FeKiLh.gst_chess_board_select.value);
        oaAmdc();
    };

    function OcappP() {
        if (aPMNpJ == '') {
            return;
        };
        if (!CGbapk) {
            return;
        };
        if (!CGbapk.parentNode) {
            return;
        };
        if (!oOOlDn[aPMNpJ]) {
            return;
        };
        oOOlDn[aPMNpJ].pGiAAe.LHjjbf = NmbiKM(CGbapk.FeKiLh.gst_checkers_board_select.value);
        oaAmdc();
    };

    function JfFJij(DILNMg) {
        if (aPMNpJ == '') {
            return;
        };
        if (!CGbapk) {
            return;
        };
        if (!CGbapk.parentNode) {
            return;
        };
        if (!oOOlDn[aPMNpJ]) {
            return;
        };
        var FeKiLh = CGbapk.FeKiLh;
        DILNMg = NmbiKM(DILNMg);
        var InIPKb = FeKiLh.fabric_set.children;
        var bmfhpd = InIPKb.length;
        for (var fOGnCG = 0; fOGnCG < bmfhpd; fOGnCG++) {
            var fMnbiD = InIPKb[fOGnCG];
            if (fMnbiD.eDpcMa === DILNMg) {
                fMnbiD.classList.add('selected');
            } else {
                fMnbiD.classList.remove('selected');
            }
        };
        oOOlDn[aPMNpJ].pGiAAe.nOHEMd = DILNMg;
        oaAmdc();
    };

    function fmmGjc() {
        if (aPMNpJ == '') {
            return;
        };
        if (!CGbapk) {
            return;
        };
        if (!CGbapk.parentNode) {
            return;
        };
        if (!oOOlDn[aPMNpJ]) {
            return;
        };
        oOOlDn[aPMNpJ].pGiAAe.hHlnBA = NmbiKM(CGbapk.FeKiLh.gst_billiards_bg_select.value);
        oaAmdc();
    };

    function IoMcJN() {
        if (aPMNpJ == '') {
            return;
        };
        if (!CGbapk) {
            return;
        };
        if (!CGbapk.parentNode) {
            return;
        };
        if (!oOOlDn[aPMNpJ]) {
            return;
        };
        oOOlDn[aPMNpJ].pGiAAe.LIHMme = NmbiKM(CGbapk.FeKiLh.gst_billiards_effect_select.value);
        oaAmdc();
    };

    function CbPkDM(diOAaj) {
        diOAaj = NmbiKM(diOAaj) * 0.01;
        var iohDbA = 0;
        if (diOAaj < 5) {
            iohDbA = 0;
        } else if (diOAaj < 10) {
            iohDbA = 1;
        } else if (diOAaj < 25) {
            iohDbA = 2;
        } else if (diOAaj < 50) {
            iohDbA = 3;
        } else if (diOAaj < 100) {
            iohDbA = 4;
        } else if (diOAaj < 200) {
            iohDbA = 5;
        } else if (diOAaj < 300) {
            iohDbA = 6;
        } else if (diOAaj < 400) {
            iohDbA = 7;
        } else if (diOAaj < 500) {
            iohDbA = 8;
        } else if (diOAaj < 1000) {
            iohDbA = 9;
        } else if (diOAaj < 2000) {
            iohDbA = 10;
        } else if (diOAaj < 3000) {
            iohDbA = 11;
        } else if (diOAaj < 4000) {
            iohDbA = 12;
        } else if (diOAaj < 5000) {
            iohDbA = 13;
        } else if (diOAaj < 6000) {
            iohDbA = 14;
        } else if (diOAaj < 7000) {
            iohDbA = 15;
        } else if (diOAaj < 8000) {
            iohDbA = 16;
        } else if (diOAaj < 9000) {
            iohDbA = 17;
        } else if (diOAaj < 10000) {
            iohDbA = 18;
        } else {
            iohDbA = 19;
        };
        return iohDbA;
    };
    return eAeFAO;
})();
BLAZE.peoHoE = peoHoE;
var ilhJLf = 0;
var aDLECN = (function () {
    var PMFAbI = BLAZE.GetENV('PROJECT_CONTENT_URL');
    var mKEgAF = [1400, 1000];
    var KJAHhc = [6, 3];
    var NNgFnm = -28;
    var nFhIkg = 116;
    var bCBied = 36;
    var OmPPLi = [94, 94];
    var HOCLcO = 12;
    var pajMJA = 0.15;
    var ifKjBF = 0.3;
    var kBLkHE = 120;
    var eAeFAO = function (jCEMkN) {
        var AfekcP = jCEMkN;
        jCEMkN.eAeFAO = this;
        this.LcJlao = 0;
        this.jHIGoB = false;
        this.kIHhDL = false;
        this.FmOnAi = function (PeejaG, eCcOkf, CjncJN) {
            return AfekcP.FmOnAi(PeejaG, eCcOkf, CjncJN);
        };
        this.kiPEEd = function () {
            AfekcP.kiPEEd();
        };
        this.KDJcda = function (MlomAd) {
            AfekcP.KDJcda(MlomAd);
        };
        this.hIFbom = function () {
            AfekcP.hIFbom();
        };
        this.jpAJGd = function () {
            AfekcP.jpAJGd();
        };
        this.MchKjg = function () {
            AfekcP.MchKjg();
        };
        this.jJNMeA = function (HLkCLj) {
            AfekcP.jJNMeA(HLkCLj);
        };
        this.ccMhlO = function (ANFEbB) {
            AfekcP.ccMhlO(ANFEbB);
        };
        this.loNDBD = function (CGnGMk) {
            AfekcP.loNDBD(CGnGMk);
        };
        this.iDGbPe = function (PDipmG) {
            AfekcP.iDGbPe(PDipmG);
        };
    };
    var JpMdFf = function (lIomEJ) {
        this.fkpbbL(lIomEJ);
    };
    JpMdFf.prototype.fkpbbL = function (lIomEJ) {
        if (lIomEJ.length < 2) {
            $error(20819591);
            return;
        };
        if (this.AIIHhG) {
            $error(20819592);
            return;
        };
        if (!EEJefK(lIomEJ[0])) {
            $error(20819593);
            return;
        };
        if (lIomEJ[1]) {
            ilhJLf = 1;
        } else {
            ilhJLf = 0;
        };
        this.eAeFAO = null;
        this.jJIAdD = BLAZE.nhjLnH.fnKEDK();
        this.hBeflg = false;
        this.gnaGcc();
        this.AIIHhG = lIomEJ[0];
        this.Biabka = null;
        this.bDnigP = null;
        this.aaPLhk = null;
        this.BkoHcI = null;
        this.AfePkf = new BLAZE.EejcjF('ChessRenderer', mKEgAF[1], mKEgAF[1], 1, ilhJLf);
        this.AfePkf.acfdaJ = true;
        this.AfePkf.KdieCl = false;
        this.AfePkf.IPPmOm = false;
        this.AfePkf.IgMlEF.CClMcd = true;
        this.LcdpGp = BLAZE.nhjLnH.oAclpm('element', 'game.chess_table');
        if (!this.LcdpGp) {
            $error(63950928);
            return;
        };
        ggGkJc.ikDpkl(this.LcdpGp);
        this.LcdpGp.KJkiNL = true;
        var McEjlk = this.LcdpGp.FeKiLh;
        var AFmnNn = McEjlk.table_sectors;
        var fOGnCG = 0;
        for (var IHAHdd = 0; IHAHdd < 8; IHAHdd++) {
            var AhiPNJ = document.createElement('div');
            AhiPNJ.className = 'ChessTableRow';
            AhiPNJ.imODiM = this;
            AFmnNn.appendChild(AhiPNJ);
            for (var GnpGgM = 0; GnpGgM < 8; GnpGgM++) {
                var fMnbiD = BLAZE.nhjLnH.MlaAIK('game.chess_sector', false);
                fMnbiD.pcDEfk = fOGnCG;
                AhiPNJ.appendChild(fMnbiD);
                McEjlk['s_' + fOGnCG] = fMnbiD;
                McEjlk['a_' + fOGnCG] = fMnbiD;
                fOGnCG++;
            }
        };
        AFmnNn.addEventListener('touchend', this.JnNiaM, true);
        AFmnNn.addEventListener('touchstart', this.JnNiaM, true);
        AFmnNn.addEventListener('mouseup', this.JnNiaM, true);
        AFmnNn.addEventListener('mousedown', this.JnNiaM, true);
        this.MglooE = BLAZE.nhjLnH.oAclpm('element', 'game.chess_select');
        this.npicEG = BLAZE.nhjLnH.oAclpm('element', 'game.chess_flash');
        var GmbpEk = this;
    };
    JpMdFf.prototype.FmOnAi = function (PeejaG, eCcOkf, CjncJN) {
        if (!this.AIIHhG) {
            $warn(2290681);
            return false;
        };
        if (this.hBeflg) {
            $warn(2290682);
            return false;
        };
        if (!PeejaG) {
            $warn(2290683);
            return false;
        };
        if (!eCcOkf) {
            $warn(2290684);
            return false;
        };
        var DnMOJK = 0;
        if (CjncJN) {
            DnMOJK = 1;
        };
        if (ilhJLf != DnMOJK) {
            ilhJLf = DnMOJK;
            this.AfePkf.nbpblG();
            this.AfePkf.jNdIig();
            this.AfePkf = new BLAZE.EejcjF('ChessRenderer', mKEgAF[1], mKEgAF[1], 1, ilhJLf);
            this.AfePkf.acfdaJ = true;
            this.AfePkf.KdieCl = false;
            this.AfePkf.IPPmOm = false;
            this.AfePkf.IgMlEF.CClMcd = true;
        };
        this.eAeFAO.LcJlao = 0;
        this.gnaGcc();
        if (eCcOkf.length != 11) {
            $warn(64223638);
            return false;
        };
        eCcOkf[2] = NmbiKM(eCcOkf[2]);
        eCcOkf[3] = NmbiKM(eCcOkf[3]);
        eCcOkf[4] = NmbiKM(eCcOkf[4]);
        eCcOkf[5] = NmbiKM(eCcOkf[5]);
        eCcOkf[6] = NmbiKM(eCcOkf[6]);
        eCcOkf[7] = NmbiKM(eCcOkf[7]);
        this.BJoBNk = eCcOkf;
        this.mJEfnh = eCcOkf[5] == 1;
        this.Biabka = PeejaG;
        var FeKiLh = this.Biabka.FeKiLh;
        this.OlGPmN = PeejaG.parentNode;
        if (!this.OlGPmN) {
            $error(95882103);
            return;
        };
        this.KcMlaa = ggGkJc.oAcDfp(this.OlGPmN);
        this.bDnigP = FeKiLh.GameScoreboard;
        this.aaPLhk = FeKiLh.GameArea;
        this.lBFeil = FeKiLh.GameFullZone;
        this.BkoHcI = FeKiLh.GameTable;
        this.BkoHcI.appendChild(this.LcdpGp);
        this.AfePkf.bGanCM(this.BkoHcI);
        this.AIIHhG.ojJMoF(mKEgAF, false);
        this.iIKgJL(eCcOkf[7], eCcOkf[8]);
        this.hBeflg = true;
        return true;
    };
    JpMdFf.prototype.kiPEEd = function () {
        if (!this.AIIHhG) {
            $warn(59029918);
            return;
        };
        this.BlECiI(1, '');
        this.BlECiI(2, '');
        this.lMDGph([]);
        this.BkkBGK();
        this.gnaGcc();
        this.hBeflg = false;
        if (this.MglooE) {
            if (this.MglooE.parentNode) {
                this.MglooE.parentNode.removeChild(this.MglooE);
            }
        };
        if (this.npicEG) {
            if (this.npicEG.parentNode) {
                this.npicEG.parentNode.removeChild(this.npicEG);
            }
        };
        if (this.LcdpGp) {
            if (this.LcdpGp.parentNode) {
                this.LcdpGp.parentNode.removeChild(this.LcdpGp);
            }
        };
        if (this.AfePkf) {
            this.AfePkf.jNdIig();
            this.AfePkf.pAKJck();
        };
        this.Biabka = null;
        this.bDnigP = null;
        this.aaPLhk = null;
        this.BkoHcI = null;
    };
    JpMdFf.prototype.MchKjg = function () {
        this.kiPEEd();
        this.AIIHhG = null;
        this.MglooE = null;
        this.npicEG = null;
        this.LcdpGp = null;
        this.AfePkf = null;
    };
    JpMdFf.prototype.gnaGcc = function () {
        this.NMoCbi = {};
        this.NMoCbi._6 = [[[-1, 0]], [[1, 0]], [[0, -1]], [[0, 1]], [[-1, -1]], [[1, 1]], [[1, -1]], [[-1, 1]]];
        this.NMoCbi._5 = [[[-1, 0], [-2, 0], [-3, 0], [-4, 0], [-5, 0], [-6, 0], [-7, 0]], [[0, -1], [0, -2], [0, -3], [0, -4], [0, -5], [0, -6], [0, -7]], [[1, 0], [2, 0], [3, 0], [4, 0], [5, 0], [6, 0], [7, 0]], [[0, 1], [0, 2], [0, 3], [0, 4], [0, 5], [0, 6], [0, 7]], [[-1, -1], [-2, -2], [-3, -3], [-4, -4], [-5, -5], [-6, -6], [-7, -7]], [[1, -1], [2, -2], [3, -3], [4, -4], [5, -5], [6, -6], [7, -7]], [[-1, 1], [-2, 2], [-3, 3], [-4, 4], [-5, 5], [-6, 6], [-7, 7]], [[1, 1], [2, 2], [3, 3], [4, 4], [5, 5], [6, 6], [7, 7]]];
        this.NMoCbi._4 = [[[-1, -1], [-2, -2], [-3, -3], [-4, -4], [-5, -5], [-6, -6], [-7, -7]], [[1, -1], [2, -2], [3, -3], [4, -4], [5, -5], [6, -6], [7, -7]], [[-1, 1], [-2, 2], [-3, 3], [-4, 4], [-5, 5], [-6, 6], [-7, 7]], [[1, 1], [2, 2], [3, 3], [4, 4], [5, 5], [6, 6], [7, 7]]];
        this.NMoCbi._3 = [[[-2, 1]], [[-2, -1]], [[2, -1]], [[2, 1]], [[-1, -2]], [[1, -2]], [[-1, 2]], [[1, 2]]];
        this.NMoCbi._2 = [[[-1, 0], [-2, 0], [-3, 0], [-4, 0], [-5, 0], [-6, 0], [-7, 0]], [[0, -1], [0, -2], [0, -3], [0, -4], [0, -5], [0, -6], [0, -7]], [[1, 0], [2, 0], [3, 0], [4, 0], [5, 0], [6, 0], [7, 0]], [[0, 1], [0, 2], [0, 3], [0, 4], [0, 5], [0, 6], [0, 7]]];
        this.NMoCbi._1W = [[[1, 0]]];
        this.NMoCbi._1WF = [[[1, 0], [2, 0]]];
        this.NMoCbi._1WC = [[[1, -1]], [[1, 1]]];
        this.NMoCbi._1B = [[[-1, 0]]];
        this.NMoCbi._1BF = [[[-1, 0], [-2, 0]]];
        this.NMoCbi._1BC = [[[-1, -1]], [[-1, 1]]];
        this.dCLkjM = null;
        this.eLHmnH = false;
        this.LlCjig = 0;
        this.ImnNgj = '';
        this.BJoBNk = null;
        this.mJEfnh = false;
        this.CaPgMf = {
            _1: [],
            _2: []
        };
        this.CnokOK = [];
        this.BidDIf = [];
        this.GJCkgG = 1.0;
        this.chkefF = null;
        this.mHLpEl = 0;
        this.dNHMpc = 0;
        this.JnhGOm = false;
        this.kaLPng = 0;
        this.Npkhdf = 0;
        this.lfbBml = null;
        this.MAnAPL = [];
        this.NEeENj = [];
        this.JJckDd = [];
        this.hCljaI = -1;
        this.dDfmCJ = '';
        this.bLpagB = '';
        this.JCaDMM = null;
        this.CcHlaF = null;
        this.NgPjGI = {};
        this.LfjDoB = {};
        this.CAKjCD = null;
        this.JaDHiB = {};
        this.jhbgjk = '';
        this.PlMEmA = null;
        this.ohHoOa = false;
        this.EiIkmG = 0;
        this.jjDfaE = -1;
        this.jaBFEF = [];
        this.kJGCli = null;
        this.BiiEId = '';
        this.joEnMj = -1;
        this.MJEPlf = null;
        this.JOCPJN = null;
        this.kFlNgO = 0;
        this.POBAKo = 0;
        this.hlMcjF = 0;
        this.GmcLeF = 0;
        this.LgPhAh = null;
        this.IkOPfg = 0;
        this.OiilAB = false;
    };
    JpMdFf.prototype.ccMhlO = function (ANFEbB) {
        if (!this.hBeflg) {
            return;
        };
        if (this.LcdpGp) {
            var oeigjE = this.LcdpGp.FeKiLh;
            var IgMlEF = oeigjE.gEMMMF;
            if (!IgMlEF) {
                IgMlEF = oeigjE.table_super_game;
                if (IgMlEF.parentNode) {
                    IgMlEF.parentNode.removeChild(IgMlEF);
                };
                this.BkoHcI.appendChild(IgMlEF);
                oeigjE.gEMMMF = IgMlEF;
            };
            var oeigjE = this.LcdpGp.FeKiLh;
            oeigjE.table_super_game_zp.innerHTML = ANFEbB + ' ZP';
            IgMlEF.classList.add('AnimSuperGame');
        }
    };
    JpMdFf.prototype.iDGbPe = function (MpONGN) {
        if (!this.hBeflg) {
            return;
        };
        var MBllBn, DILNMg, PDipmG;
        this.KcMlaa = ggGkJc.oAcDfp(this.OlGPmN);
        this.LoELbN = ggGkJc.oAcDfp(this.aadigp);
        MpONGN[0] -= MpONGN[0] % 8;
        MpONGN[1] -= MpONGN[1] % 8;
        var OIgcNj = MpONGN[0] + 'px';
        var LapKCP = MpONGN[1] + 'px';
        var fcKPoC = '';
        var IGLNPh = '';
        var pKcabG = '';
        var pjfEHf = MpONGN[0] >= MpONGN[1];
        if (pjfEHf) {
            fcKPoC = MpONGN[1] + 'px';
            IGLNPh = '0px';
            pKcabG = Math.round((MpONGN[0] - MpONGN[1]) * 0.5) + 'px';
            this.GJCkgG = MpONGN[0] / mKEgAF[0];
        } else {
            fcKPoC = MpONGN[0] + 'px';
            IGLNPh = Math.round((MpONGN[1] - MpONGN[0]) * 0.5) + 'px';
            pKcabG = '0px';
            this.GJCkgG = MpONGN[1] / mKEgAF[0];
        };
        var s, l;
        if (this.LcdpGp) {
            s = this.LcdpGp.style;
            s.width = s.height = fcKPoC;
            s.top = IGLNPh;
            s.left = pKcabG;
            var McEjlk = this.LcdpGp.FeKiLh;
            McEjlk.table_sectors.style.padding = Math.round(bCBied * this.GJCkgG) + 'px';
            var OgaDGl = 0.85;
            var kHOLhl = this.GJCkgG * OgaDGl;
            var DBgGAA = Math.round((mKEgAF[0] - mKEgAF[1]) * 0.5);
            var fnffHN, aehhLb, ejINnI;
            if (pjfEHf) {
                fnffHN = Math.round(DBgGAA / OgaDGl) + 'px';
                aehhLb = Math.round(mKEgAF[1] / OgaDGl) + 'px';
            } else {
                fnffHN = Math.round(mKEgAF[1] / OgaDGl) + 'px';
                aehhLb = Math.round(DBgGAA / OgaDGl) + 'px';
            };
            l = McEjlk.stack_2.classList;
            s = McEjlk.stack_2.style;
            s.width = fnffHN;
            s.height = aehhLb;
            if (pjfEHf) {
                l.remove('StackPortrait');
                l.add('StackLandscape');
                s.top = '0px';
                s.left = '-' + fnffHN;
                ggGkJc.GlmmOC(McEjlk.stack_2, kHOLhl, kHOLhl);
            } else {
                l.add('StackPortrait');
                l.remove('StackLandscape');
                s.top = '0px';
                s.left = '0px';
                ggGkJc.GlmmOC(McEjlk.stack_2, kHOLhl, -kHOLhl);
            };
            l = McEjlk.stack_1.classList;
            s = McEjlk.stack_1.style;
            s.width = fnffHN;
            s.height = aehhLb;
            if (pjfEHf) {
                l.remove('StackPortrait');
                l.add('StackLandscape');
                s.top = '0px';
                s.bottom = '';
                s.left = '';
                s.right = '-' + fnffHN;
            } else {
                l.add('StackPortrait');
                l.remove('StackLandscape');
                s.top = '';
                s.bottom = '-' + aehhLb;
                s.left = '0px';
                s.right = '';
            };
            ggGkJc.GlmmOC(McEjlk.stack_1, kHOLhl, kHOLhl);
        };
        if (this.AfePkf) {
            s = this.AfePkf.IgMlEF.style;
            s.width = s.height = fcKPoC;
            s.top = IGLNPh;
            s.left = pKcabG;
        };
        this.nOjkce();
    };
    JpMdFf.prototype.KDJcda = function (MlomAd) {
        if (!MlomAd) {
            return;
        };
        this.eLHmnH = false;
        this.dCLkjM = MlomAd;
        this.dCLkjM.HolCMn = 0;
        if (this.chkefF !== null) {
            window.clearTimeout(this.chkefF);
        };
        this.chkefF = window.setTimeout(this.pAinAi, 50, this);
    };
    JpMdFf.prototype.hIFbom = function () {
        if (!this.dCLkjM) {
            return;
        };
        if (this.chkefF !== null) {
            window.clearTimeout(this.chkefF);
        };
        this.AIIHhG.OgInlJ();
        this.eLHmnH = false;
        this.dCLkjM.HolCMn = 0;
        this.chkefF = window.setTimeout(this.pAinAi, 50, this);
    };
    JpMdFf.prototype.oODIpi = function () {
        if (!this.dCLkjM) {
            return;
        };
        if (this.dCLkjM.HolCMn >= this.dCLkjM.MplMCo.length - 1) {
            return;
        };
        if (this.chkefF !== null) {
            window.clearTimeout(this.chkefF);
        };
        this.eLHmnH = true;
        this.AIIHhG.JJJgMI();
        this.AIIHhG.NBPlhb();
        this.AIIHhG.HjGcOh();
    };
    JpMdFf.prototype.jpAJGd = function () {
        if (!this.dCLkjM) {
            return;
        };
        if (this.chkefF !== null) {
            window.clearTimeout(this.chkefF);
        };
        this.eLHmnH = false;
        this.AIIHhG.afPMfG();
        this.eopFHf();
    };
    JpMdFf.prototype.eopFHf = function () {
        if (!this.dCLkjM) {
            return;
        };
        if (this.ohHoOa || this.eLHmnH) {
            return;
        };
        if (this.chkefF !== null) {
            window.clearTimeout(this.chkefF);
        };
        var cNPiod = 1500;
        if (this.dCLkjM.HolCMn < 1) {
            cNPiod = 50;
        };
        this.chkefF = window.setTimeout(this.dhiiJb, cNPiod, this);
    };
    JpMdFf.prototype.pAinAi = function (EgNgBG) {
        if (!EgNgBG.dCLkjM || !EgNgBG.hBeflg) {
            return;
        };
        EgNgBG.cFaPCi();
    };
    JpMdFf.prototype.dhiiJb = function (EgNgBG) {
        if (!EgNgBG.dCLkjM || !EgNgBG.hBeflg) {
            return;
        };
        if (this.ohHoOa || this.eLHmnH) {
            return;
        };
        var HolCMn = EgNgBG.dCLkjM.HolCMn;
        var MplMCo = EgNgBG.dCLkjM.MplMCo;
        if (HolCMn < MplMCo.length) {
            var fMnbiD = MplMCo[HolCMn];
            HolCMn = HolCMn + 1;
            EgNgBG.dCLkjM.HolCMn = HolCMn;
            EgNgBG.jJNMeA(fMnbiD);
        } else {
            EgNgBG.AIIHhG.afPMfG();
        }
    };
    JpMdFf.prototype.cFaPCi = function () {
        if (!this.hBeflg) {
            return;
        };
        var DILNMg, MBllBn, fOGnCG, bmfhpd, HIhniL, MlomAd, hoMDEC;
        var hCHoIl = false;
        if (this.CnokOK.length > 0) {
            MlomAd = this.CnokOK.shift();
            hoMDEC = MlomAd[0];
            if (hoMDEC == 'i') {
                this.ImnNgj = MlomAd[1];
                this.AIIHhG.geEeHn();
                this.lMDGph([]);
                this.BkkBGK();
                this.ohHoOa = false;
                this.jaBFEF = [];
                hCHoIl = true;
                this.PnlGBG();
            } else if (hoMDEC == 's') {
                DILNMg = MlomAd[1].split(',');
                if (DILNMg.length == 2) {
                    MBllBn = NmbiKM(DILNMg[0]);
                    this.JCaDMM = BLAZE.nhjLnH.oAclpm('bitmap', 'chess_figures_' + MBllBn);
                    if (MBllBn == 0) {
                        this.dDfmCJ = 'chks_0_';
                    } else {
                        this.dDfmCJ = 'chss_' + MBllBn + '_';
                    };
                    MBllBn = NmbiKM(DILNMg[1]);
                    this.CcHlaF = BLAZE.nhjLnH.oAclpm('bitmap', 'chess_figures_' + MBllBn);
                    if (MBllBn == 0) {
                        this.bLpagB = 'chks_0_';
                    } else {
                        this.bLpagB = 'chss_' + MBllBn + '_';
                    }
                };
                if (this.ohHoOa) {
                    this.jhbgjk = MlomAd[2];
                } else {
                    this.fcNGMI(MlomAd[2]);
                }
            } else if (hoMDEC == 'a') {
                this.dNHMpc = NmbiKM(MlomAd[2]);
                this.mHLpEl = NmbiKM(MlomAd[1]);
                this.JnhGOm = false;
                this.kaLPng = 0;
                this.Npkhdf = 0;
                this.lMDGph([]);
                this.BkkBGK();
                this.CAKjCD = null;
                this.JaDHiB = {};
                this.AIIHhG.gFepJD();
                this.NEeENj = [];
                if (MlomAd[3] != '') {
                    HIhniL = MlomAd[3].split(',');
                    bmfhpd = HIhniL.length;
                    for (fOGnCG = 0; fOGnCG < bmfhpd; fOGnCG++) {
                        MBllBn = HIhniL[fOGnCG].split('_');
                        if (MBllBn.length == 3) {
                            this.NEeENj.push([NmbiKM(MBllBn[0]), NmbiKM(MBllBn[1]), NmbiKM(MBllBn[2])]);
                        }
                    };
                };
                this.JJckDd = [];
                if (MlomAd[4] != '') {
                    HIhniL = MlomAd[4].split(',');
                    bmfhpd = HIhniL.length;
                    for (fOGnCG = 0; fOGnCG < bmfhpd; fOGnCG++) {
                        this.JJckDd['_' + HIhniL[fOGnCG]] = true;
                    }
                };
            } else if (hoMDEC == 'r') {
                this.JnhGOm = false;
                this.mHLpEl = 0;
                this.kaLPng = 0;
                this.Npkhdf = 0;
                this.lMDGph([]);
                this.BkkBGK();
                this.CAKjCD = null;
                this.JaDHiB = {};
                this.AIIHhG.HamnNA();
            } else if (hoMDEC == 'p') {
                var HLiMHP = NmbiKM(MlomAd[1]);
                if ((this.eAeFAO.LcJlao != HLiMHP && HLiMHP > 0) || !this.eAeFAO.jHIGoB) {
                    this.dNHMpc = NmbiKM(MlomAd[3]);
                    var jgkIma = [[NmbiKM(MlomAd[2]), NmbiKM(MlomAd[4].split(':')[0])]];
                    if (MlomAd[5] != '') {
                        HIhniL = MlomAd[5].split('_');
                        if (HIhniL.length == 2) {
                            jgkIma.push([NmbiKM(HIhniL[0]), NmbiKM(HIhniL[1]), true]);
                        }
                    };
                    this.dfEdDm(jgkIma);
                }
            } else {
                $warn('GC ' + hoMDEC);
            }
        };
        if (this.BidDIf.length > 0 && !hCHoIl) {
            this.AIIHhG.OgInlJ();
            var pKaopF = this.BidDIf.shift();
            var LeNpNP = HAELdp.OHokFB(knJbka() - pKaopF[0]);
            MlomAd = pKaopF[1];
            var bmfhpd = MlomAd.length;
            for (var fOGnCG = 0; fOGnCG < bmfhpd; fOGnCG++) {
                DILNMg = MlomAd[fOGnCG].split('#');
                hoMDEC = DILNMg[0];
                if (hoMDEC == 'p') {
                    if (DILNMg.length < 4) {
                        this.AIIHhG.MHIJhF(DILNMg[1], GbiMej('computer_player'), DILNMg[3]);
                    } else {
                        this.AIIHhG.MHIJhF(DILNMg[1], DILNMg[2], DILNMg[3]);
                    }
                } else if (hoMDEC == 's') {} else if (hoMDEC == 'i') {
                    this.AIIHhG.odcMgf(DILNMg[1], DILNMg[2]);
                } else if (hoMDEC == 'h') {
                    this.BlECiI(DILNMg[1], DILNMg[2]);
                } else if (hoMDEC == 'j') {
                    this.emfbLG(DILNMg[1], DILNMg[2]);
                } else if (hoMDEC == 'c') {
                    this.AIIHhG.haNiCk(DILNMg[1]);
                } else if (hoMDEC == 't') {
                    this.AIIHhG.CdFBij(NmbiKM(DILNMg[1]) + LeNpNP, DILNMg[2]);
                } else if (hoMDEC == 'e') {
                    this.AIIHhG.jBilmk(DILNMg[1]);
                } else if (hoMDEC == 'r') {
                    this.AIIHhG.FJEcfm(DILNMg[1], NmbiKM(DILNMg[2]) + LeNpNP);
                } else if (hoMDEC == 'w') {
                    this.AIIHhG.HjGcOh();
                    if (this.ohHoOa) {
                        this.PlMEmA = DILNMg;
                    } else {
                        this.JnhGOm = false;
                        this.mHLpEl = 0;
                        this.kaLPng = 0;
                        this.Npkhdf = 0;
                        this.lMDGph([]);
                        this.BkkBGK();
                        this.CAKjCD = null;
                        this.JaDHiB = {};
                        this.AIIHhG.HjGcOh();
                        this.AIIHhG.aBNniF(DILNMg[1], DILNMg[2], DILNMg[3], DILNMg[4], DILNMg[5], DILNMg[6]);
                        this.PlMEmA = null;
                    }
                } else if (hoMDEC == 'v') {
                    this.AIIHhG.gHDccP();
                    var FPNbFH = DILNMg.length;
                    for (var jGfFPE = 1; jGfFPE < FPNbFH; jGfFPE++) {
                        this.AIIHhG.MBnfai(DILNMg[jGfFPE]);
                    }
                } else if (hoMDEC == 'l') {
                    this.AIIHhG.MBnfai(DILNMg[1]);
                } else {
                    $warn('IC ' + hoMDEC);
                }
            };
        };
        if (this.CnokOK.length > 0 || this.BidDIf.length > 0) {
            this.cFaPCi();
        } else if (this.dCLkjM) {
            this.eopFHf();
        }
    };
    JpMdFf.prototype.jJNMeA = function (HLkCLj) {
        if (!this.hBeflg) {
            return;
        };
        if (!HLkCLj) {
            return;
        };
        if (HLkCLj.hasOwnProperty('gcn')) {
            this.AIIHhG.Ilmieb();
        };
        if (HLkCLj.hasOwnProperty('cpi')) {
            this.eAeFAO.LcJlao = NmbiKM(HLkCLj['cpi']);
        };
        var hKbcfc = false;
        if (HLkCLj.hasOwnProperty('gv')) {
            hKbcfc = true;
            var InIPKb = String(HLkCLj.gv).split('|');
            var bmfhpd = InIPKb.length;
            for (var fOGnCG = 0; fOGnCG < bmfhpd; fOGnCG++) {
                var AGbLFh = InIPKb[fOGnCG].split('#');
                var iMKLlL = AGbLFh[0];
                this.CnokOK.push(AGbLFh);
            }
        };
        if (HLkCLj.hasOwnProperty('gs')) {
            hKbcfc = true;
            this.BidDIf.push([knJbka(), String(HLkCLj.gs).split('|')]);
        };
        if (!this.cnaFhk && hKbcfc) {
            this.cFaPCi();
        }
    };
    JpMdFf.prototype.loNDBD = function (CGnGMk) {
        if (!this.hBeflg) {
            return;
        };
        this.fFMLbJ();
    };
    JpMdFf.prototype.iIKgJL = function (GmbBoJ, kcAcbf) {
        GmbBoJ = NmbiKM(GmbBoJ);
        kcAcbf = NmbiKM(kcAcbf);
        this.LlCjig = ejHLnG();
        this.AfePkf.nbpblG();
        this.LfjDoB = {};
        var McEjlk = this.LcdpGp.FeKiLh;
        McEjlk.table_default.style.backgroundImage = 'url("' + BLAZE.nhjLnH.oAclpm('bitmap', 'chess_default_table').src + '")';
        McEjlk.table_overlay.classList.remove('transition');
        McEjlk.table_overlay.style.backgroundImage = 'none';
        if (GmbBoJ > 0) {
            McEjlk.table_overlay.style.display = 'block';
            McEjlk.table_overlay.style.opacity = '0';
            var pKaopF = 'chb' + GmbBoJ;
            BLAZE.nhjLnH.dkgJMA(pKaopF, PMFAbI + pKaopF + '.png?' + BLAZE.CONTENT_VERSION, 1, this.kgEkDP, this);
        } else {
            McEjlk.table_overlay.style.display = 'none';
        }
    };
    JpMdFf.prototype.NKeAKN = function () {
        return (ejHLnG() - this.LlCjig) < 1000;
    };
    JpMdFf.prototype.kgEkDP = function (BiAKPf, aCKfgg, pMdaFp) {
        if (!pMdaFp || !aCKfgg) {
            return;
        };
        if (!pMdaFp.LcdpGp) {
            return;
        };
        var IgMlEF = pMdaFp.LcdpGp.FeKiLh.table_overlay;
        IgMlEF.style.backgroundImage = 'url("' + aCKfgg.src + '")';
        if (!pMdaFp.NKeAKN()) {
            IgMlEF.classList.add('transition');
        };
        IgMlEF.style.opacity = '1';
    };
    JpMdFf.prototype.fcNGMI = function (kOPkdE) {
        this.CAKjCD = null;
        this.JaDHiB = {};
        this.jhbgjk = '';
        if (!this.hBeflg) {
            return;
        };
        if (!this.LcdpGp) {
            return;
        };
        var McEjlk = this.LcdpGp.FeKiLh;
        if (this.hCljaI != this.eAeFAO.LcJlao) {
            this.hCljaI = this.eAeFAO.LcJlao;
            if (this.hCljaI == 1 || this.hCljaI == 2) {
                McEjlk.table_base.classList.remove('FlipBoard');
                McEjlk.table_numbers.style.backgroundImage = 'url("' + BLAZE.nhjLnH.oAclpm('bitmap', 'chess_numbers_' + this.hCljaI).src + '")';
            } else {
                McEjlk.table_base.classList.add('FlipBoard');
                McEjlk.table_numbers.style.backgroundImage = 'url("' + BLAZE.nhjLnH.oAclpm('bitmap', 'chess_numbers_0').src + '")';
            };
            var DILNMg;
            var AFmnNn = McEjlk.table_sectors;
            for (var fOGnCG = 0; fOGnCG < 64; fOGnCG++) {
                var fMnbiD = McEjlk['s_' + fOGnCG];
                var pcDEfk = fOGnCG;
                var LFOfEg = pcDEfk % 8;
                var KLPIak = (pcDEfk - LFOfEg) / 8;
                if (this.hCljaI == 1) {
                    DILNMg = KLPIak;
                    KLPIak = LFOfEg;
                    LFOfEg = 7 - DILNMg;
                } else if (this.hCljaI == 2) {
                    DILNMg = KLPIak;
                    KLPIak = 7 - LFOfEg;
                    LFOfEg = DILNMg;
                };
                pcDEfk = KLPIak * 8 + LFOfEg;
                McEjlk['a_' + pcDEfk] = fMnbiD;
            }
        };
        this.lMDGph([]);
        this.BkkBGK();
        this.ohHoOa = false;
        this.jaBFEF = [];
        var cblkjL = Object.keys(this.NgPjGI);
        this.NgPjGI = {};
        var InIPKb = kOPkdE.split(';');
        var gbaffp, HIhniL, fOGnCG, bmfhpd = InIPKb.length;
        for (fOGnCG = 0; fOGnCG < bmfhpd; fOGnCG++) {
            HIhniL = InIPKb[fOGnCG].split(':');
            if (HIhniL.length == 2) {
                this.NgPjGI['_' + NmbiKM(HIhniL[0])] = [NmbiKM(HIhniL[1]), 0];
            } else if (HIhniL.length == 3) {
                this.NgPjGI['_' + NmbiKM(HIhniL[0])] = [NmbiKM(HIhniL[1]), NmbiKM(HIhniL[2])];
            }
        };
        var JhECmA = '';
        var oeigjE = cblkjL.length;
        for (fOGnCG = 0; fOGnCG < oeigjE; fOGnCG++) {
            gbaffp = cblkjL[fOGnCG];
            if (!this.NgPjGI[gbaffp]) {
                HIhniL = NmbiKM(gbaffp.substring(1));
                if (HIhniL >= 1 && HIhniL <= 8) {
                    JhECmA = this.bLpagB;
                } else if (HIhniL >= 21 && HIhniL <= 28) {
                    JhECmA = this.dDfmCJ;
                }
            };
        };
        if (JhECmA != '') {
            if (this.hBeflg && this.LcdpGp && bmfhpd > 0) {
                JMBDGp.gDicAB(JhECmA + 'kill', 1, false, 0, true);
            }
        };
        this.nOjkce();
        this.fmggND(1);
        this.fmggND(2);
    };
    JpMdFf.prototype.PnlGBG = function () {
        this.NgPjGI = {};
        this.nOjkce();
    };
    JpMdFf.prototype.nOjkce = function () {
        if (!this.hBeflg) {
            return;
        };
        if (!this.LcdpGp) {
            return;
        };
        if (this.hCljaI < 0) {
            return;
        };
        var APNChP, FhhdPP;
        for (APNChP in this.NgPjGI) {
            var FhhdPP = NmbiKM(APNChP.substring(1));
            var lfhCNa = FhhdPP < 21;
            var IgMlEF = this.LfjDoB[APNChP];
            if (!IgMlEF) {
                if (lfhCNa) {
                    IgMlEF = new BLAZE.BKaEgK(this.JCaDMM, 1, 4, KJAHhc);
                    IgMlEF.igHPal = new BLAZE.BKaEgK(this.JCaDMM, 1, 4, KJAHhc);
                } else {
                    IgMlEF = new BLAZE.BKaEgK(this.CcHlaF, 1, 4, KJAHhc);
                    IgMlEF.igHPal = new BLAZE.BKaEgK(this.JCaDMM, 1, 4, KJAHhc);
                };
                IgMlEF.mcnbao(-1, IgMlEF.igHPal);
                this.AfePkf.mcnbao(-1, IgMlEF);
                this.LfjDoB[APNChP] = IgMlEF;
            };
            var NLCnnI = FhhdPP % 20;
            if (this.NgPjGI[APNChP][1] > 0) {
                NLCnnI = 15;
            };
            if (NLCnnI == 16) {
                NLCnnI = 0;
            } else if (NLCnnI == 15) {
                NLCnnI = 1;
            } else if (NLCnnI >= 13) {
                NLCnnI = 2;
            } else if (NLCnnI >= 11) {
                NLCnnI = 3;
            } else if (NLCnnI >= 9) {
                NLCnnI = 4;
            } else {
                NLCnnI = 5;
            };
            IgMlEF.igHPal.eHEgIc(NLCnnI + 12);
            if (!lfhCNa) {
                NLCnnI = NLCnnI + 6;
            };
            IgMlEF.eHEgIc(NLCnnI);
            lJELmO.cJJPaG(this.gNJJlP(this.NgPjGI[APNChP][0]), this.LfjDoB[APNChP].AcPOPM);
        };
        var mJeAlE = Object.keys(this.LfjDoB);
        var bmfhpd = mJeAlE.length;
        for (var fOGnCG = 0; fOGnCG < bmfhpd; fOGnCG++) {
            APNChP = mJeAlE[fOGnCG];
            if (!this.NgPjGI.hasOwnProperty(APNChP)) {
                this.AfePkf.anCblL(this.LfjDoB[APNChP]);
                delete this.LfjDoB[APNChP];
            }
        };
        this.AfePkf.aGcIfL();
    };
    JpMdFf.prototype.CGFGmI = function (AcPOPM) {
        var DILNMg;
        var LFOfEg = Math.round(Math.floor(AcPOPM[0] / nFhIkg));
        var KLPIak = Math.round(Math.floor(AcPOPM[1] / nFhIkg));
        if (this.hCljaI == 1) {
            DILNMg = KLPIak;
            KLPIak = LFOfEg;
            LFOfEg = 7 - DILNMg;
        } else if (this.hCljaI == 2) {
            DILNMg = KLPIak;
            KLPIak = 7 - LFOfEg;
            LFOfEg = DILNMg;
        };
        return [LFOfEg, KLPIak];
    };
    JpMdFf.prototype.MAgcCp = function (AcPOPM) {
        var DILNMg;
        var LFOfEg = Math.round(Math.floor(AcPOPM[0] / nFhIkg));
        var KLPIak = Math.round(Math.floor(AcPOPM[1] / nFhIkg));
        if (this.hCljaI == 1) {
            DILNMg = KLPIak;
            KLPIak = LFOfEg;
            LFOfEg = 7 - DILNMg;
        } else if (this.hCljaI == 2) {
            DILNMg = KLPIak;
            KLPIak = 7 - LFOfEg;
            LFOfEg = DILNMg;
        };
        return Math.round(LFOfEg + (KLPIak * 8));
    };
    JpMdFf.prototype.bNNnfJ = function (pcDEfk) {
        var LFOfEg = pcDEfk % 8;
        var KLPIak = (pcDEfk - LFOfEg) / 8;
        return [LFOfEg, KLPIak];
    };
    JpMdFf.prototype.gNJJlP = function (pcDEfk) {
        var DILNMg;
        var LFOfEg = pcDEfk % 8;
        var KLPIak = (pcDEfk - LFOfEg) / 8;
        if (this.hCljaI == 1) {
            DILNMg = KLPIak;
            KLPIak = 7 - LFOfEg;
            LFOfEg = DILNMg;
        } else if (this.hCljaI == 2) {
            DILNMg = KLPIak;
            KLPIak = LFOfEg;
            LFOfEg = 7 - DILNMg;
        };
        return [(LFOfEg * nFhIkg) + OmPPLi[0], (KLPIak * nFhIkg) + OmPPLi[1] + NNgFnm];
    };
    JpMdFf.prototype.IlaoKI = function (pcDEfk) {
        var LFOfEg = pcDEfk % 8;
        var KLPIak = (pcDEfk - LFOfEg) / 8;
        if (KLPIak % 2 == 0) {
            return LFOfEg % 2 != 0;
        } else {
            return LFOfEg % 2 == 0;
        }
    };
    JpMdFf.prototype.BlECiI = function (dKglFf, MlomAd) {
        if (!this.LcdpGp) {
            return;
        };
        if (dKglFf != 1 && dKglFf != 2) {
            return;
        };
        this.CaPgMf['_' + dKglFf] = [];
        this.emfbLG(dKglFf, MlomAd);
    };
    JpMdFf.prototype.emfbLG = function (dKglFf, MlomAd) {
        if (!this.LcdpGp) {
            return;
        };
        if (dKglFf != 1 && dKglFf != 2) {
            return;
        };
        var JlbiDa = this.CaPgMf['_' + dKglFf];
        var HIhniL = MlomAd.split(':');
        var bmfhpd = HIhniL.length;
        for (var fOGnCG = 0; fOGnCG < bmfhpd; fOGnCG++) {
            var DILNMg = HIhniL[fOGnCG].split('.');
            if (DILNMg.length == 2) {
                JlbiDa.push([NmbiKM(DILNMg[0]), NmbiKM(DILNMg[1])]);
            }
        };
        this.fmggND(dKglFf);
    };
    JpMdFf.prototype.fmggND = function (dKglFf) {
        if (!this.LcdpGp) {
            return;
        };
        if (!this.JCaDMM || !this.CcHlaF) {
            return;
        };
        var Biabka;
        var ljCiCc = '';
        if (this.hCljaI == 1) {
            if (dKglFf == 1) {
                ljCiCc = 'url("' + this.CcHlaF.src + '")';
                Biabka = this.LcdpGp.FeKiLh['stack_1'];
            } else if (dKglFf == 2) {
                ljCiCc = 'url("' + this.JCaDMM.src + '")';
                Biabka = this.LcdpGp.FeKiLh['stack_2'];
            } else {
                return;
            }
        } else if (this.hCljaI == 2) {
            if (dKglFf == 1) {
                ljCiCc = 'url("' + this.CcHlaF.src + '")';
                Biabka = this.LcdpGp.FeKiLh['stack_2'];
            } else if (dKglFf == 2) {
                ljCiCc = 'url("' + this.JCaDMM.src + '")';
                Biabka = this.LcdpGp.FeKiLh['stack_1'];
            } else {
                return;
            }
        } else {
            if (dKglFf == 1) {
                ljCiCc = 'url("' + this.CcHlaF.src + '")';
                Biabka = this.LcdpGp.FeKiLh['stack_2'];
            } else if (dKglFf == 2) {
                ljCiCc = 'url("' + this.JCaDMM.src + '")';
                Biabka = this.LcdpGp.FeKiLh['stack_1'];
            } else {
                return;
            }
        };
        var JlbiDa = this.CaPgMf['_' + dKglFf];
        var IgMlEF, bmfhpd = JlbiDa.length;
        for (var fOGnCG = 0; fOGnCG < HOCLcO; fOGnCG++) {
            var jaNIpg = 'S' + fOGnCG;
            var GCmDhM = 'E' + fOGnCG;
            if (fOGnCG >= bmfhpd) {
                IgMlEF = Biabka[GCmDhM];
                if (IgMlEF) {
                    if (IgMlEF.parentNode) {
                        IgMlEF.parentNode.removeChild(IgMlEF);
                    };
                    IgMlEF = null;
                    delete Biabka[GCmDhM];
                };
                IgMlEF = Biabka[jaNIpg];
                if (IgMlEF) {
                    if (IgMlEF.parentNode) {
                        IgMlEF.parentNode.removeChild(IgMlEF);
                    };
                    IgMlEF = null;
                    delete Biabka[jaNIpg];
                }
            } else {
                var DILNMg = JlbiDa[fOGnCG];
                var lfhCNa = DILNMg[0] < 21;
                var NLCnnI = DILNMg[0] % 20;
                if (DILNMg[1] > 0) {
                    NLCnnI = 15;
                };
                if (NLCnnI == 16) {
                    NLCnnI = 0;
                } else if (NLCnnI == 15) {
                    NLCnnI = 1;
                } else if (NLCnnI >= 13) {
                    NLCnnI = 2;
                } else if (NLCnnI >= 11) {
                    NLCnnI = 3;
                } else if (NLCnnI >= 9) {
                    NLCnnI = 4;
                } else {
                    NLCnnI = 5;
                };
                IgMlEF = Biabka[jaNIpg];
                if (!IgMlEF) {
                    IgMlEF = document.createElement('div');
                    Biabka[jaNIpg] = IgMlEF;
                    Biabka.appendChild(IgMlEF);
                };
                IgMlEF.style.backgroundImage = ljCiCc;
                IgMlEF.className = 'ChessShadow Frame' + (NLCnnI + 12);
                IgMlEF = Biabka[GCmDhM];
                if (!IgMlEF) {
                    IgMlEF = document.createElement('div');
                    Biabka[GCmDhM] = IgMlEF;
                    Biabka[jaNIpg].appendChild(IgMlEF);
                };
                IgMlEF.style.backgroundImage = ljCiCc;
                if (lfhCNa) {
                    IgMlEF.className = 'ChessFigure Frame' + NLCnnI;
                } else {
                    IgMlEF.className = 'ChessFigure Frame' + (NLCnnI + 6);
                }
            };
        }
    };
    JpMdFf.prototype.JDaDFO = function (pcDEfk) {
        if (!this.LcdpGp || !this.MglooE) {
            return;
        };
        this.BkkBGK();
        if (this.MglooE.parentNode) {
            this.MglooE.parentNode.removeChild(this.MglooE);
        };
        this.MglooE.classList.remove('Transition');
        this.MglooE.style.opacity = 1;
        var McEjlk = this.LcdpGp.FeKiLh;
        var hJBOIC = 'a_' + pcDEfk;
        if (!McEjlk[hJBOIC]) {
            return;
        };
        McEjlk[hJBOIC].appendChild(this.MglooE);
    };
    JpMdFf.prototype.BkkBGK = function () {
        if (this.MglooE) {
            this.MglooE.classList.add('Transition');
            this.MglooE.style.opacity = 0;
        }
    };
    JpMdFf.prototype.fhKaMP = function (pcDEfk) {
        if (!this.LcdpGp || !this.npicEG) {
            return;
        };
        if (this.npicEG.parentNode) {
            this.npicEG.parentNode.removeChild(this.npicEG);
        };
        var McEjlk = this.LcdpGp.FeKiLh;
        var hJBOIC = 'a_' + pcDEfk;
        if (!McEjlk[hJBOIC]) {
            return;
        };
        McEjlk[hJBOIC].appendChild(this.npicEG);
        this.npicEG.style.display = 'none';
        this.npicEG.classList.remove('Animation');
        this.npicEG.style.display = '';
        this.npicEG.classList.add('Animation');
    };
    JpMdFf.prototype.lMDGph = function (AFmnNn) {
        if (!this.LcdpGp) {
            return;
        };
        var McEjlk = this.LcdpGp.FeKiLh;
        var NcdPLc = {};
        var fOGnCG, bmfhpd = AFmnNn.length;
        for (fOGnCG = 0; fOGnCG < bmfhpd; fOGnCG++) {
            NcdPLc['_' + AFmnNn[fOGnCG]] = true;
        };
        for (fOGnCG = 0; fOGnCG < 64; fOGnCG++) {
            var fMnbiD = McEjlk['a_' + fOGnCG];
            if (fMnbiD) {
                if (NcdPLc['_' + fOGnCG]) {
                    if (this.IlaoKI(fOGnCG)) {
                        fMnbiD.classList.add('CH_White');
                    } else {
                        fMnbiD.classList.add('CH_Black');
                    }
                } else {
                    fMnbiD.classList.remove('CH_Black');
                    fMnbiD.classList.remove('CH_White');
                }
            };
        }
    };
    JpMdFf.prototype.PAdmoJ = function (FhhdPP, cfagom) {
        if (!cfagom) {
            return;
        };
        if (!this.hBeflg) {
            return;
        };
        var khkhcP = [];
        var bmfhpd = cfagom.length;
        for (var fOGnCG = 0; fOGnCG < bmfhpd; fOGnCG++) {
            khkhcP.push([FhhdPP, NmbiKM(cfagom[fOGnCG])]);
        };
        this.dfEdDm(khkhcP);
    };
    JpMdFf.prototype.dfEdDm = function (khkhcP) {
        if (!khkhcP) {
            return;
        };
        if (!this.hBeflg) {
            return;
        };
        if (this.ohHoOa) {
            var bmfhpd = this.jaBFEF.length;
            for (var fOGnCG = 0; fOGnCG < bmfhpd; fOGnCG++) {
                var fCmCdh = this.jaBFEF[fOGnCG];
                var APNChP = '_' + fCmCdh[0];
                var pBOFOj = NmbiKM(fCmCdh[1]) % 64;
                if (this.LfjDoB[APNChP]) {
                    this.LfjDoB[APNChP].AcPOPM = this.gNJJlP(pBOFOj);
                }
            };
            this.AfePkf.aGcIfL();
        };
        this.ohHoOa = true;
        this.jaBFEF = khkhcP;
        this.IFnEGf();
    };
    JpMdFf.prototype.IFnEGf = function () {
        if (!this.hBeflg || !this.ohHoOa) {
            return;
        };
        var HHNLkp;
        if (this.BiiEId != '') {
            if (this.LfjDoB[this.BiiEId]) {
                this.AfePkf.anCblL(this.LfjDoB[this.BiiEId]);
                delete this.LfjDoB[this.BiiEId];
            };
            this.BiiEId = '';
        };
        if (this.jjDfaE > 20) {
            HHNLkp = this.bLpagB;
        } else {
            HHNLkp = this.dDfmCJ;
        };
        if (this.jjDfaE > 0) {
            if (this.OiilAB) {
                JMBDGp.gDicAB(HHNLkp + 'hit', 1, false, 0, true);
            }
        };
        if (this.jaBFEF.length < 1) {
            if (this.kJGCli) {
                this.AfePkf.KIDCEI();
                this.AfePkf.lgNAAi();
                this.kJGCli.igHPal.HilidP = true;
                this.kJGCli = null;
            };
            this.jjDfaE = -1;
            this.ohHoOa = false;
            if (this.jhbgjk != '') {
                this.fcNGMI(this.jhbgjk);
            } else {
                this.AfePkf.aGcIfL();
            };
            if (this.JnhGOm) {
                if (this.lfbBml) {
                    if (this.mJEfnh) {
                        this.lMDGph(this.lfbBml.AFmnNn);
                    }
                };
            };
            if (this.PlMEmA) {
                this.JnhGOm = false;
                this.mHLpEl = 0;
                this.kaLPng = 0;
                this.Npkhdf = 0;
                this.lMDGph([]);
                this.BkkBGK();
                this.CAKjCD = null;
                this.JaDHiB = {};
                this.AIIHhG.HjGcOh();
                this.AIIHhG.aBNniF(this.PlMEmA[1], this.PlMEmA[2], this.PlMEmA[3], this.PlMEmA[4], this.PlMEmA[5], this.PlMEmA[6]);
                this.PlMEmA = null;
            };
            if (this.dCLkjM) {
                this.eopFHf();
            }
        } else {
            var fCmCdh = this.jaBFEF.shift();
            var APNChP = '_' + fCmCdh[0];
            var pBOFOj = NmbiKM(fCmCdh[1]) % 64;
            if (this.LfjDoB[APNChP]) {
                if (!this.JnhGOm) {
                    this.fhKaMP(pBOFOj);
                };
                this.ohHoOa = true;
                this.jjDfaE = fCmCdh[0];
                this.BiiEId = '';
                this.kJGCli = this.LfjDoB[APNChP];
                this.joEnMj = pBOFOj;
                this.JOCPJN = this.gNJJlP(pBOFOj);
                this.MJEPlf = lJELmO.NoeNdn(this.kJGCli.AcPOPM);
                this.LgPhAh = lJELmO.khOMcp(this.JOCPJN, this.MJEPlf);
                this.kFlNgO = lJELmO.PaaKha(this.LgPhAh);
                this.POBAKo = this.kFlNgO * 0.5;
                this.IkOPfg = 1 / this.POBAKo / this.POBAKo;
                this.hlMcjF = 0;
                this.GmcLeF = 0;
                if (fCmCdh.length > 2) {
                    this.OiilAB = true;
                } else {
                    this.OiilAB = this.jjDfaE % 20;
                    this.OiilAB = this.OiilAB == 11 || this.OiilAB == 12;
                };
                if (this.kFlNgO / nFhIkg > 1.9) {
                    this.EiIkmG = ifKjBF;
                } else {
                    this.EiIkmG = pajMJA;
                };
                var fOGnCG, dgLdGd;
                var cfiLMN = {};
                for (var kdbnIl in this.NgPjGI) {
                    if (this.NgPjGI[kdbnIl][0] == pBOFOj) {
                        this.BiiEId = kdbnIl;
                        break;
                    }
                };
                if (this.jjDfaE > 20) {
                    HHNLkp = this.bLpagB;
                } else {
                    HHNLkp = this.dDfmCJ;
                };
                this.AfePkf.LfFMlG(this.kJGCli);
                if (this.OiilAB) {
                    this.kJGCli.igHPal.HilidP = false;
                } else {
                    this.kJGCli.igHPal.HilidP = true;
                    JMBDGp.gDicAB(HHNLkp + 'move', 1, false, 0, true);
                };
                if (this.BiiEId != '') {
                    var MKjgcC = NmbiKM(this.BiiEId.substring(1));
                    if (MKjgcC < 21) {
                        HHNLkp = this.bLpagB;
                    } else {
                        HHNLkp = this.dDfmCJ;
                    };
                    JMBDGp.gDicAB(HHNLkp + 'kill', 1, false, 0, true);
                }
            } else {
                this.IFnEGf();
            }
        };
    };
    JpMdFf.prototype.fFMLbJ = function () {
        if (!this.ohHoOa) {
            return;
        };
        if (this.kJGCli) {
            this.hlMcjF = this.hlMcjF + BLAZE.paIPdi.KeOOoA;
            if (this.hlMcjF < this.EiIkmG) {
                this.GmcLeF = (this.hlMcjF / this.EiIkmG) * this.kFlNgO;
                var akdcAH = lJELmO.PAGKnH(this.LgPhAh, this.GmcLeF / this.kFlNgO);
                lJELmO.jeDgdF(akdcAH, this.MJEPlf);
                if (this.OiilAB) {
                    var EhoLJF = Math.abs(this.GmcLeF - this.POBAKo);
                    EhoLJF = kBLkHE - (kBLkHE * EhoLJF * EhoLJF * this.IkOPfg);
                    akdcAH[1] = akdcAH[1] - EhoLJF;
                };
                this.kJGCli.AcPOPM = akdcAH;
                this.AfePkf.aGcIfL();
                return;
            };
            this.kJGCli.AcPOPM = this.JOCPJN;
        };
        this.IFnEGf();
        this.AfePkf.aGcIfL();
    };
    JpMdFf.prototype.JnNiaM = function (EAmjJJ) {
        var IgMlEF = EAmjJJ.target;
        if (EAmjJJ.type == 'touchend') {
            if (EAmjJJ.changedTouches.length < 1) {
                return;
            };
            var lboAhk = EAmjJJ.changedTouches[0];
            EAmjJJ.preventDefault();
            EAmjJJ.stopPropagation();
            IgMlEF = document.elementFromPoint(lboAhk.clientX, lboAhk.clientY);
        } else if (EAmjJJ.type == 'touchstart') {
            EAmjJJ.preventDefault();
            EAmjJJ.stopPropagation();
        };
        if (!IgMlEF) {
            return;
        };
        if (!IgMlEF.parentNode) {
            return;
        };
        if (!IgMlEF.parentNode.imODiM) {
            return;
        };
        IgMlEF.parentNode.imODiM.oJfEFP(EAmjJJ.type, IgMlEF.pcDEfk);
    };
    JpMdFf.prototype.oJfEFP = function (dFlGoB, pcDEfk) {
        if (this.dCLkjM) {
            this.oODIpi();
            return;
        };
        if (!this.hBeflg || !this.eAeFAO.jHIGoB || this.ohHoOa || this.mHLpEl < 1) {
            return;
        };
        pcDEfk = NmbiKM(pcDEfk);
        var DILNMg, HHNLkp, fOGnCG, bmfhpd;
        var LFOfEg = pcDEfk % 8;
        var KLPIak = (pcDEfk - LFOfEg) / 8;
        if (this.hCljaI == 1) {
            DILNMg = KLPIak;
            KLPIak = LFOfEg;
            LFOfEg = 7 - DILNMg;
        } else if (this.hCljaI == 2) {
            DILNMg = KLPIak;
            KLPIak = 7 - LFOfEg;
            LFOfEg = DILNMg;
        };
        pcDEfk = KLPIak * 8 + LFOfEg;
        var FhhdPP = 0;
        for (var APNChP in this.NgPjGI) {
            if (this.NgPjGI[APNChP][0] == pcDEfk) {
                FhhdPP = NmbiKM(APNChP.substring(1));
                break;
            }
        };
        this.bIJNNo(this.mHLpEl);
        if (this.kaLPng == 0) {
            if (dFlGoB == 'mousedown' || dFlGoB == 'touchstart') {
                if (FhhdPP > 0) {
                    if (this.mHLpEl == 1) {
                        if (FhhdPP > 20) {
                            return;
                        };
                        HHNLkp = this.dDfmCJ;
                    } else if (this.mHLpEl == 2) {
                        if (FhhdPP < 21) {
                            return;
                        };
                        HHNLkp = this.bLpagB;
                    } else {
                        return;
                    };
                    JMBDGp.gDicAB(HHNLkp + 'click', 1, false, 0, true);
                    this.MAnAPL = [];
                    this.kaLPng = FhhdPP;
                    this.Npkhdf = pcDEfk;
                    this.JDaDFO(pcDEfk);
                    this.lfbBml = this.PaNDGP(this.kaLPng);
                    if (this.mJEfnh) {
                        this.lMDGph(this.lfbBml.AFmnNn);
                    }
                };
            }
        } else {
            if (dFlGoB == 'mousedown' || dFlGoB == 'touchstart') {
                if (!this.JnhGOm) {
                    if (this.kaLPng == FhhdPP || this.Npkhdf == pcDEfk) {} else {
                        if (FhhdPP > 0) {
                            if (this.mHLpEl == 1) {
                                if (FhhdPP > 20) {
                                    return;
                                };
                                HHNLkp = this.dDfmCJ;
                            } else if (this.mHLpEl == 2) {
                                if (FhhdPP < 21) {
                                    return;
                                };
                                HHNLkp = this.bLpagB;
                            } else {
                                return;
                            };
                            this.MAnAPL = [];
                            this.kaLPng = FhhdPP;
                            this.Npkhdf = pcDEfk;
                            this.JDaDFO(pcDEfk);
                            this.lfbBml = this.PaNDGP(this.kaLPng);
                            if (this.mJEfnh) {
                                this.lMDGph(this.lfbBml.AFmnNn);
                            };
                            JMBDGp.gDicAB(HHNLkp + 'click', 1, false, 0, true);
                        }
                    };
                }
            } else if (dFlGoB == 'mouseup' || dFlGoB == 'touchend') {
                if (this.lfbBml) {
                    var HbnLBg = '_' + pcDEfk;
                    if (this.lfbBml.hasOwnProperty(HbnLBg)) {
                        this.MAnAPL.push(pcDEfk);
                        this.lMDGph([]);
                        var jgkIma = [[this.kaLPng, pcDEfk]];
                        if (this.kaLPng == 16 || this.kaLPng == 36) {
                            bmfhpd = this.NEeENj.length;
                            for (fOGnCG = 0; fOGnCG < bmfhpd; fOGnCG++) {
                                var MIfKDH = this.NEeENj[fOGnCG];
                                if (pcDEfk == MIfKDH[1]) {
                                    jgkIma.push([MIfKDH[0], MIfKDH[2], true]);
                                }
                            };
                        };
                        this.dfEdDm(jgkIma);
                        var fpMgcJ = this.lfbBml[HbnLBg];
                        if (fpMgcJ > 0) {
                            fpMgcJ = '_' + fpMgcJ;
                            if (this.NgPjGI[fpMgcJ]) {
                                delete this.NgPjGI[fpMgcJ];
                            }
                        };
                        this.NgPjGI['_' + this.kaLPng][0] = pcDEfk;
                        this.lfbBml = null;
                        this.CAKjCD = null;
                        this.JaDHiB = {};
                        this.mHLpEl = 0;
                        this.BkkBGK();
                        this.AIIHhG.DJMNpK({
                            c: 'move',
                            v: this.kaLPng + ':' + this.MAnAPL.join(':')
                        });
                        this.MAnAPL = [];
                        this.AIIHhG.HamnNA();
                    }
                };
            }
        };
    };
    JpMdFf.prototype.PaNDGP = function (FhhdPP) {
        if (this.CAKjCD) {
            var APNChP = '_' + FhhdPP;
            if (this.CAKjCD[APNChP]) {
                return this.CAKjCD[APNChP];
            }
        };
        return {
            AFmnNn: []
        };
    };
    JpMdFf.prototype.bIJNNo = function (kIKhFD) {
        if (this.CAKjCD) {
            return;
        };
        this.CAKjCD = {};
        this.JaDHiB = {};
        var fOGnCG, bmfhpd, APNChP, FhhdPP;
        var IBpkAb = [];
        var KkpKfc = [];
        var cfiLMN = {};
        for (APNChP in this.NgPjGI) {
            FhhdPP = NmbiKM(APNChP.substring(1));
            cfiLMN['_' + this.NgPjGI[APNChP][0]] = FhhdPP;
            if (kIKhFD == 1) {
                if (FhhdPP < 21) {
                    IBpkAb.push(FhhdPP);
                    continue;
                }
            } else {
                if (FhhdPP > 20) {
                    IBpkAb.push(FhhdPP);
                    continue;
                }
            };
            KkpKfc.push(FhhdPP);
        };
        bmfhpd = KkpKfc.length;
        for (fOGnCG = 0; fOGnCG < bmfhpd; fOGnCG++) {
            FhhdPP = KkpKfc[fOGnCG];
            APNChP = '_' + FhhdPP;
            this.dkGAAH(FhhdPP, cfiLMN, true);
        };
        bmfhpd = IBpkAb.length;
        for (fOGnCG = 0; fOGnCG < bmfhpd; fOGnCG++) {
            FhhdPP = IBpkAb[fOGnCG];
            APNChP = '_' + FhhdPP;
            this.CAKjCD[APNChP] = this.dkGAAH(FhhdPP, cfiLMN, false);
        };
        bmfhpd = KkpKfc.length;
        var fIdkBN = Object.keys(this.CAKjCD);
        var oeigjE = fIdkBN.length;
        for (var PbPcJh = 0; PbPcJh < oeigjE; PbPcJh++) {
            APNChP = fIdkBN[PbPcJh];
            FhhdPP = NmbiKM(APNChP.substring(1));
            var dJMcDC = this.CAKjCD[APNChP];
            var IEEebi = {
                AFmnNn: []
            };
            for (var dgLdGd in dJMcDC) {
                var lGjFpn = NmbiKM(dgLdGd.substring(1));
                if (dgLdGd[0] == '_') {
                    var EEdEIp = 0;
                    var JMjbkM = this.lbalMi(cfiLMN, FhhdPP);
                    if (JMjbkM.hasOwnProperty(dgLdGd)) {
                        EEdEIp = JMjbkM[dgLdGd];
                    };
                    JMjbkM[dgLdGd] = FhhdPP;
                    var ACjnbj = false;
                    for (fOGnCG = 0; fOGnCG < bmfhpd; fOGnCG++) {
                        if (EEdEIp != KkpKfc[fOGnCG]) {
                            var khkhcP = this.dkGAAH(KkpKfc[fOGnCG], JMjbkM, false);
                            if (khkhcP.ACjnbj) {
                                ACjnbj = true;
                                break;
                            }
                        };
                    };
                    if (ACjnbj) {
                        continue;
                    };
                    IEEebi[dgLdGd] = dJMcDC[dgLdGd];
                    IEEebi.AFmnNn.push(lGjFpn);
                }
            };
            if (IEEebi.AFmnNn.length > 0) {
                this.CAKjCD[APNChP] = IEEebi;
            } else {
                delete this.CAKjCD[APNChP];
            }
        };
    };
    JpMdFf.prototype.dkGAAH = function (FhhdPP, cfiLMN, lJnFmG) {
        var fOGnCG, bmfhpd, kdbnIl, PbPcJh, MIfKDH, dgLdGd, lGjFpn, APNChP, llIIgc, EhoLJF;
        var KmngMC = this.BJoBNk[1];
        var khkhcP = {
            AFmnNn: [],
            ACjnbj: false
        };
        APNChP = '_' + FhhdPP;
        if (!this.NgPjGI[APNChP]) {
            return khkhcP;
        };
        var NdlloI = this.NgPjGI[APNChP][0];
        var hENPHg = this.bNNnfJ(NdlloI);
        var difnaM = false;
        var lfhCNa = FhhdPP < 21;
        var jBFdkl, paEjmJ;
        var LLGLjd = FhhdPP % 20;
        if (this.NgPjGI[APNChP][1] > 0) {
            LLGLjd = 15;
        };
        var FffFeb = null;
        var KOiiJO = null;
        if (LLGLjd == 16) {
            difnaM = true;
            FffFeb = this.NMoCbi._6;
        } else if (LLGLjd == 15) {
            FffFeb = this.NMoCbi._5;
        } else if (LLGLjd >= 13) {
            FffFeb = this.NMoCbi._4;
        } else if (LLGLjd >= 11) {
            FffFeb = this.NMoCbi._3;
        } else if (LLGLjd >= 9) {
            FffFeb = this.NMoCbi._2;
        } else {
            if (lfhCNa) {
                if (hENPHg[0] == 1) {
                    FffFeb = this.NMoCbi._1WF;
                } else {
                    FffFeb = this.NMoCbi._1W;
                };
                KOiiJO = this.NMoCbi._1WC;
            } else {
                if (hENPHg[0] == 6) {
                    FffFeb = this.NMoCbi._1BF;
                } else {
                    FffFeb = this.NMoCbi._1B;
                };
                KOiiJO = this.NMoCbi._1BC;
            }
        };
        if (difnaM && !lJnFmG) {
            bmfhpd = this.NEeENj.length;
            for (fOGnCG = 0; fOGnCG < bmfhpd; fOGnCG++) {
                MIfKDH = this.NEeENj[fOGnCG];
                lGjFpn = MIfKDH[1];
                khkhcP['_' + lGjFpn] = MIfKDH[0];
                khkhcP.AFmnNn.push(lGjFpn);
            }
        };
        var jmjcnk = FffFeb.length;
        for (PbPcJh = 0; PbPcJh < jmjcnk; PbPcJh++) {
            MIfKDH = FffFeb[PbPcJh];
            bmfhpd = MIfKDH.length;
            for (fOGnCG = 0; fOGnCG < bmfhpd; fOGnCG++) {
                llIIgc = lJELmO.mCMKjO(hENPHg, MIfKDH[fOGnCG]);
                if (llIIgc[0] < 0 || llIIgc[0] > 7) {
                    continue;
                };
                if (llIIgc[1] < 0 || llIIgc[1] > 7) {
                    continue;
                };
                lGjFpn = llIIgc[1] * 8 + llIIgc[0];
                dgLdGd = '_' + lGjFpn;
                if (difnaM && !lJnFmG) {
                    if (this.JaDHiB[dgLdGd]) {
                        break;
                    }
                };
                if (!cfiLMN.hasOwnProperty(dgLdGd)) {
                    if (lJnFmG && !KOiiJO) {
                        this.JaDHiB[dgLdGd] = true;
                    };
                    khkhcP[dgLdGd] = 0;
                    khkhcP.AFmnNn.push(lGjFpn);
                } else if (KOiiJO) {
                    break;
                } else {
                    kdbnIl = cfiLMN[dgLdGd];
                    if (this.NgPjGI['_' + kdbnIl]) {
                        if (lfhCNa && kdbnIl < 21) {} else if (!lfhCNa && kdbnIl > 20) {} else {
                            if (lJnFmG && !KOiiJO) {
                                this.JaDHiB[dgLdGd] = true;
                            };
                            khkhcP[dgLdGd] = kdbnIl;
                            khkhcP.AFmnNn.push(lGjFpn);
                            if (kdbnIl == 16 || kdbnIl == 36) {
                                khkhcP.ACjnbj = true;
                            }
                        };
                        break;
                    }
                };
            }
        };
        if (KOiiJO) {
            jmjcnk = KOiiJO.length;
            for (PbPcJh = 0; PbPcJh < jmjcnk; PbPcJh++) {
                MIfKDH = KOiiJO[PbPcJh];
                bmfhpd = MIfKDH.length;
                for (fOGnCG = 0; fOGnCG < bmfhpd; fOGnCG++) {
                    llIIgc = lJELmO.mCMKjO(hENPHg, MIfKDH[fOGnCG]);
                    if (llIIgc[0] < 0 || llIIgc[0] > 7) {
                        continue;
                    };
                    if (llIIgc[1] < 0 || llIIgc[1] > 7) {
                        continue;
                    };
                    lGjFpn = llIIgc[1] * 8 + llIIgc[0];
                    dgLdGd = '_' + lGjFpn;
                    if (!cfiLMN.hasOwnProperty(dgLdGd)) {
                        if (lJnFmG) {
                            this.JaDHiB[dgLdGd] = true;
                        };
                        break;
                    } else {
                        kdbnIl = cfiLMN[dgLdGd];
                        if (this.NgPjGI['_' + kdbnIl]) {
                            if (lfhCNa && kdbnIl < 21) {} else if (!lfhCNa && kdbnIl > 20) {} else {
                                if (lJnFmG) {
                                    this.JaDHiB[dgLdGd] = true;
                                };
                                khkhcP[dgLdGd] = kdbnIl;
                                khkhcP.AFmnNn.push(lGjFpn);
                                if (kdbnIl == 16 || kdbnIl == 36) {
                                    khkhcP.ACjnbj = true;
                                }
                            };
                            break;
                        }
                    };
                }
            };
            FffFeb = [[0, 1], [0, -1]];
            jmjcnk = FffFeb.length;
            for (fOGnCG = 0; fOGnCG < jmjcnk; fOGnCG++) {
                llIIgc = lJELmO.mCMKjO(hENPHg, FffFeb[fOGnCG]);
                if (llIIgc[0] < 0 || llIIgc[0] > 7) {
                    continue;
                };
                if (llIIgc[1] < 0 || llIIgc[1] > 7) {
                    continue;
                };
                lGjFpn = llIIgc[1] * 8 + llIIgc[0];
                dgLdGd = '_' + lGjFpn;
                if (cfiLMN.hasOwnProperty(dgLdGd)) {
                    kdbnIl = cfiLMN[dgLdGd];
                    if (this.JJckDd['_' + kdbnIl]) {
                        if (lfhCNa) {
                            llIIgc[0] = llIIgc[0] + 1;
                        } else {
                            llIIgc[0] = llIIgc[0] - 1;
                        };
                        lGjFpn = llIIgc[1] * 8 + llIIgc[0];
                        dgLdGd = '_' + lGjFpn;
                        if (!cfiLMN.hasOwnProperty(dgLdGd)) {
                            khkhcP[dgLdGd] = 999;
                            khkhcP.AFmnNn.push(lGjFpn);
                        }
                    };
                }
            };
        };
        return khkhcP;
    };
    JpMdFf.prototype.lbalMi = function (cfiLMN, fDdGbp) {
        var JMjbkM = {};
        for (var pcDEfk in cfiLMN) {
            var FhhdPP = cfiLMN[pcDEfk];
            if (fDdGbp != FhhdPP) {
                JMjbkM[pcDEfk] = FhhdPP;
            }
        };
        return JMjbkM;
    };
    return function () {
        return new eAeFAO(new JpMdFf(arguments))
    };
})();
BLAZE.aDLECN = aDLECN;
var GoaAhe = (function () {
    var PMFAbI = BLAZE.GetENV('PROJECT_CONTENT_URL');
    var mKEgAF = [1400, 1000];
    var KJAHhc = [2, 3];
    var nFhIkg = 116;
    var bCBied = 36;
    var OmPPLi = [94, 94];
    var HOCLcO = 12;
    var pajMJA = 0.15;
    var ifKjBF = 0.3;
    var kBLkHE = 120;
    var eAeFAO = function (jCEMkN) {
        var AfekcP = jCEMkN;
        jCEMkN.eAeFAO = this;
        this.LcJlao = 0;
        this.jHIGoB = false;
        this.kIHhDL = false;
        this.FmOnAi = function (PeejaG, eCcOkf, CjncJN) {
            return AfekcP.FmOnAi(PeejaG, eCcOkf, CjncJN);
        };
        this.kiPEEd = function () {
            AfekcP.kiPEEd();
        };
        this.KDJcda = function (MlomAd) {
            AfekcP.KDJcda(MlomAd);
        };
        this.hIFbom = function () {
            AfekcP.hIFbom();
        };
        this.jpAJGd = function () {
            AfekcP.jpAJGd();
        };
        this.MchKjg = function () {
            AfekcP.MchKjg();
        };
        this.jJNMeA = function (HLkCLj) {
            AfekcP.jJNMeA(HLkCLj);
        };
        this.ccMhlO = function (ANFEbB) {
            AfekcP.ccMhlO(ANFEbB);
        };
        this.loNDBD = function (CGnGMk) {
            AfekcP.loNDBD(CGnGMk);
        };
        this.iDGbPe = function (PDipmG) {
            AfekcP.iDGbPe(PDipmG);
        };
    };
    var JpMdFf = function (lIomEJ) {
        this.fkpbbL(lIomEJ);
    };
    JpMdFf.prototype.fkpbbL = function (lIomEJ) {
        if (lIomEJ.length < 2) {
            $error(20819591);
            return;
        };
        if (this.AIIHhG) {
            $error(20819592);
            return;
        };
        if (!EEJefK(lIomEJ[0])) {
            $error(20819593);
            return;
        };
        if (lIomEJ[1]) {
            ilhJLf = 1;
        } else {
            ilhJLf = 0;
        };
        this.eAeFAO = null;
        this.jJIAdD = BLAZE.nhjLnH.fnKEDK();
        this.hBeflg = false;
        this.gnaGcc();
        this.AIIHhG = lIomEJ[0];
        this.Biabka = null;
        this.bDnigP = null;
        this.aaPLhk = null;
        this.BkoHcI = null;
        this.AfePkf = new BLAZE.EejcjF('ChessRenderer', mKEgAF[1], mKEgAF[1], 1, ilhJLf);
        this.AfePkf.acfdaJ = true;
        this.AfePkf.KdieCl = false;
        this.AfePkf.IPPmOm = false;
        this.AfePkf.IgMlEF.CClMcd = true;
        this.LcdpGp = BLAZE.nhjLnH.oAclpm('element', 'game.checkers_table');
        if (!this.LcdpGp) {
            $error(63950928);
            return;
        };
        ggGkJc.ikDpkl(this.LcdpGp);
        this.LcdpGp.KJkiNL = true;
        var McEjlk = this.LcdpGp.FeKiLh;
        var AFmnNn = McEjlk.table_sectors;
        var fOGnCG = 0;
        for (var IHAHdd = 0; IHAHdd < 8; IHAHdd++) {
            var AhiPNJ = document.createElement('div');
            AhiPNJ.className = 'ChessTableRow';
            AhiPNJ.imODiM = this;
            AFmnNn.appendChild(AhiPNJ);
            for (var GnpGgM = 0; GnpGgM < 8; GnpGgM++) {
                var fMnbiD = BLAZE.nhjLnH.MlaAIK('game.checkers_sector', false);
                fMnbiD.pcDEfk = fOGnCG;
                AhiPNJ.appendChild(fMnbiD);
                McEjlk['s_' + fOGnCG] = fMnbiD;
                McEjlk['a_' + fOGnCG] = fMnbiD;
                fOGnCG++;
            }
        };
        AFmnNn.addEventListener('touchend', this.JnNiaM, true);
        AFmnNn.addEventListener('touchstart', this.JnNiaM, true);
        AFmnNn.addEventListener('mouseup', this.JnNiaM, true);
        AFmnNn.addEventListener('mousedown', this.JnNiaM, true);
        this.MglooE = BLAZE.nhjLnH.oAclpm('element', 'game.checkers_select');
        this.npicEG = BLAZE.nhjLnH.oAclpm('element', 'game.checkers_flash');
        var GmbpEk = this;
    };
    JpMdFf.prototype.FmOnAi = function (PeejaG, eCcOkf, CjncJN) {
        if (!this.AIIHhG) {
            $warn(2290681);
            return false;
        };
        if (this.hBeflg) {
            $warn(2290682);
            return false;
        };
        if (!PeejaG) {
            $warn(2290683);
            return false;
        };
        if (!eCcOkf) {
            $warn(2290684);
            return false;
        };
        var DnMOJK = 0;
        if (CjncJN) {
            DnMOJK = 1;
        };
        if (ilhJLf != DnMOJK) {
            ilhJLf = DnMOJK;
            this.AfePkf.nbpblG();
            this.AfePkf.jNdIig();
            this.AfePkf = new BLAZE.EejcjF('ChessRenderer', mKEgAF[1], mKEgAF[1], 1, ilhJLf);
            this.AfePkf.acfdaJ = true;
            this.AfePkf.KdieCl = false;
            this.AfePkf.IPPmOm = false;
            this.AfePkf.IgMlEF.CClMcd = true;
        };
        this.eAeFAO.LcJlao = 0;
        this.gnaGcc();
        if (eCcOkf.length != 11) {
            $warn(64223638);
            return false;
        };
        eCcOkf[2] = NmbiKM(eCcOkf[2]);
        eCcOkf[3] = NmbiKM(eCcOkf[3]);
        eCcOkf[4] = NmbiKM(eCcOkf[4]);
        eCcOkf[5] = NmbiKM(eCcOkf[5]);
        eCcOkf[6] = NmbiKM(eCcOkf[6]);
        eCcOkf[7] = NmbiKM(eCcOkf[7]);
        this.BJoBNk = eCcOkf;
        this.mJEfnh = eCcOkf[5] == 1;
        this.Biabka = PeejaG;
        var FeKiLh = this.Biabka.FeKiLh;
        this.OlGPmN = PeejaG.parentNode;
        if (!this.OlGPmN) {
            $error(95882103);
            return;
        };
        this.KcMlaa = ggGkJc.oAcDfp(this.OlGPmN);
        this.bDnigP = FeKiLh.GameScoreboard;
        this.aaPLhk = FeKiLh.GameArea;
        this.lBFeil = FeKiLh.GameFullZone;
        this.BkoHcI = FeKiLh.GameTable;
        this.BkoHcI.appendChild(this.LcdpGp);
        this.AfePkf.bGanCM(this.BkoHcI);
        this.AIIHhG.ojJMoF(mKEgAF, false);
        this.iIKgJL(eCcOkf[7], eCcOkf[8]);
        this.hBeflg = true;
        return true;
    };
    JpMdFf.prototype.kiPEEd = function () {
        if (!this.AIIHhG) {
            $warn(59029918);
            return;
        };
        this.BlECiI(1, '');
        this.BlECiI(2, '');
        this.lMDGph([]);
        this.BkkBGK();
        this.gnaGcc();
        this.hBeflg = false;
        if (this.MglooE) {
            if (this.MglooE.parentNode) {
                this.MglooE.parentNode.removeChild(this.MglooE);
            }
        };
        if (this.npicEG) {
            if (this.npicEG.parentNode) {
                this.npicEG.parentNode.removeChild(this.npicEG);
            }
        };
        if (this.LcdpGp) {
            if (this.LcdpGp.parentNode) {
                this.LcdpGp.parentNode.removeChild(this.LcdpGp);
            }
        };
        if (this.AfePkf) {
            this.AfePkf.jNdIig();
            this.AfePkf.pAKJck();
        };
        this.Biabka = null;
        this.bDnigP = null;
        this.aaPLhk = null;
        this.BkoHcI = null;
    };
    JpMdFf.prototype.MchKjg = function () {
        this.kiPEEd();
        this.AIIHhG = null;
        this.MglooE = null;
        this.npicEG = null;
        this.LcdpGp = null;
        this.AfePkf = null;
    };
    JpMdFf.prototype.gnaGcc = function () {
        this.dCLkjM = null;
        this.eLHmnH = false;
        this.LlCjig = 0;
        this.ImnNgj = '';
        this.BJoBNk = null;
        this.mJEfnh = false;
        this.CaPgMf = {
            _1: [],
            _2: []
        };
        this.CnokOK = [];
        this.BidDIf = [];
        this.GJCkgG = 1.0;
        this.chkefF = null;
        this.mHLpEl = 0;
        this.dNHMpc = 0;
        this.JnhGOm = false;
        this.kaLPng = 0;
        this.Npkhdf = 0;
        this.lfbBml = null;
        this.MAnAPL = [];
        this.hCljaI = -1;
        this.dDfmCJ = '';
        this.bLpagB = '';
        this.JCaDMM = null;
        this.CcHlaF = null;
        this.NgPjGI = {};
        this.LfjDoB = {};
        this.CAKjCD = null;
        this.jhbgjk = '';
        this.PlMEmA = null;
        this.ohHoOa = false;
        this.EiIkmG = 0;
        this.jjDfaE = -1;
        this.jaBFEF = [];
        this.kJGCli = null;
        this.BiiEId = '';
        this.joEnMj = -1;
        this.MJEPlf = null;
        this.JOCPJN = null;
        this.kFlNgO = 0;
        this.POBAKo = 0;
        this.hlMcjF = 0;
        this.GmcLeF = 0;
        this.LgPhAh = null;
        this.IkOPfg = 0;
        this.OiilAB = false;
    };
    JpMdFf.prototype.ccMhlO = function (ANFEbB) {
        if (!this.hBeflg) {
            return;
        };
        if (this.LcdpGp) {
            var oeigjE = this.LcdpGp.FeKiLh;
            var IgMlEF = oeigjE.gEMMMF;
            if (!IgMlEF) {
                IgMlEF = oeigjE.table_super_game;
                if (IgMlEF.parentNode) {
                    IgMlEF.parentNode.removeChild(IgMlEF);
                };
                this.BkoHcI.appendChild(IgMlEF);
                oeigjE.gEMMMF = IgMlEF;
            };
            var oeigjE = this.LcdpGp.FeKiLh;
            oeigjE.table_super_game_zp.innerHTML = ANFEbB + ' ZP';
            IgMlEF.classList.add('AnimSuperGame');
        }
    };
    JpMdFf.prototype.iDGbPe = function (MpONGN) {
        if (!this.hBeflg) {
            return;
        };
        var MBllBn, DILNMg, PDipmG;
        this.KcMlaa = ggGkJc.oAcDfp(this.OlGPmN);
        this.LoELbN = ggGkJc.oAcDfp(this.aadigp);
        MpONGN[0] -= MpONGN[0] % 8;
        MpONGN[1] -= MpONGN[1] % 8;
        var OIgcNj = MpONGN[0] + 'px';
        var LapKCP = MpONGN[1] + 'px';
        var fcKPoC = '';
        var IGLNPh = '';
        var pKcabG = '';
        var pjfEHf = MpONGN[0] >= MpONGN[1];
        if (pjfEHf) {
            fcKPoC = MpONGN[1] + 'px';
            IGLNPh = '0px';
            pKcabG = Math.round((MpONGN[0] - MpONGN[1]) * 0.5) + 'px';
            this.GJCkgG = MpONGN[0] / mKEgAF[0];
        } else {
            fcKPoC = MpONGN[0] + 'px';
            IGLNPh = Math.round((MpONGN[1] - MpONGN[0]) * 0.5) + 'px';
            pKcabG = '0px';
            this.GJCkgG = MpONGN[1] / mKEgAF[0];
        };
        var s, l;
        if (this.LcdpGp) {
            s = this.LcdpGp.style;
            s.width = s.height = fcKPoC;
            s.top = IGLNPh;
            s.left = pKcabG;
            var McEjlk = this.LcdpGp.FeKiLh;
            McEjlk.table_sectors.style.padding = Math.round(bCBied * this.GJCkgG) + 'px';
            var OgaDGl = 0.85;
            var kHOLhl = this.GJCkgG * OgaDGl;
            var DBgGAA = Math.round((mKEgAF[0] - mKEgAF[1]) * 0.5);
            var fnffHN, aehhLb, ejINnI;
            if (pjfEHf) {
                fnffHN = Math.round(DBgGAA / OgaDGl) + 'px';
                aehhLb = Math.round(mKEgAF[1] / OgaDGl) + 'px';
            } else {
                fnffHN = Math.round(mKEgAF[1] / OgaDGl) + 'px';
                aehhLb = Math.round(DBgGAA / OgaDGl) + 'px';
            };
            l = McEjlk.stack_2.classList;
            s = McEjlk.stack_2.style;
            s.width = fnffHN;
            s.height = aehhLb;
            if (pjfEHf) {
                l.remove('StackPortrait');
                l.add('StackLandscape');
                s.top = '0px';
                s.left = '-' + fnffHN;
                ggGkJc.GlmmOC(McEjlk.stack_2, kHOLhl, kHOLhl);
            } else {
                l.add('StackPortrait');
                l.remove('StackLandscape');
                s.top = '0px';
                s.left = '0px';
                ggGkJc.GlmmOC(McEjlk.stack_2, kHOLhl, -kHOLhl);
            };
            l = McEjlk.stack_1.classList;
            s = McEjlk.stack_1.style;
            s.width = fnffHN;
            s.height = aehhLb;
            if (pjfEHf) {
                l.remove('StackPortrait');
                l.add('StackLandscape');
                s.top = '0px';
                s.bottom = '';
                s.left = '';
                s.right = '-' + fnffHN;
            } else {
                l.add('StackPortrait');
                l.remove('StackLandscape');
                s.top = '';
                s.bottom = '-' + aehhLb;
                s.left = '0px';
                s.right = '';
            };
            ggGkJc.GlmmOC(McEjlk.stack_1, kHOLhl, kHOLhl);
        };
        if (this.AfePkf) {
            s = this.AfePkf.IgMlEF.style;
            s.width = s.height = fcKPoC;
            s.top = IGLNPh;
            s.left = pKcabG;
        };
        this.nOjkce();
    };
    JpMdFf.prototype.KDJcda = function (MlomAd) {
        if (!MlomAd) {
            return;
        };
        this.eLHmnH = false;
        this.dCLkjM = MlomAd;
        this.dCLkjM.HolCMn = 0;
        if (this.chkefF !== null) {
            window.clearTimeout(this.chkefF);
        };
        this.chkefF = window.setTimeout(this.pAinAi, 50, this);
    };
    JpMdFf.prototype.hIFbom = function () {
        if (!this.dCLkjM) {
            return;
        };
        if (this.chkefF !== null) {
            window.clearTimeout(this.chkefF);
        };
        this.AIIHhG.OgInlJ();
        this.eLHmnH = false;
        this.dCLkjM.HolCMn = 0;
        this.chkefF = window.setTimeout(this.pAinAi, 50, this);
    };
    JpMdFf.prototype.oODIpi = function () {
        if (!this.dCLkjM) {
            return;
        };
        if (this.dCLkjM.HolCMn >= this.dCLkjM.MplMCo.length - 1) {
            return;
        };
        if (this.chkefF !== null) {
            window.clearTimeout(this.chkefF);
        };
        this.eLHmnH = true;
        this.AIIHhG.JJJgMI();
        this.AIIHhG.NBPlhb();
        this.AIIHhG.HjGcOh();
    };
    JpMdFf.prototype.jpAJGd = function () {
        if (!this.dCLkjM) {
            return;
        };
        if (this.chkefF !== null) {
            window.clearTimeout(this.chkefF);
        };
        this.eLHmnH = false;
        this.AIIHhG.afPMfG();
        this.eopFHf();
    };
    JpMdFf.prototype.eopFHf = function () {
        if (!this.dCLkjM) {
            return;
        };
        if (this.ohHoOa || this.eLHmnH) {
            return;
        };
        if (this.chkefF !== null) {
            window.clearTimeout(this.chkefF);
        };
        var cNPiod = 1500;
        if (this.dCLkjM.HolCMn < 1) {
            cNPiod = 50;
        };
        this.chkefF = window.setTimeout(this.dhiiJb, cNPiod, this);
    };
    JpMdFf.prototype.pAinAi = function (EgNgBG) {
        if (!EgNgBG.dCLkjM || !EgNgBG.hBeflg) {
            return;
        };
        EgNgBG.cFaPCi();
    };
    JpMdFf.prototype.dhiiJb = function (EgNgBG) {
        if (!EgNgBG.dCLkjM || !EgNgBG.hBeflg) {
            return;
        };
        if (this.ohHoOa || this.eLHmnH) {
            return;
        };
        var HolCMn = EgNgBG.dCLkjM.HolCMn;
        var MplMCo = EgNgBG.dCLkjM.MplMCo;
        if (HolCMn < MplMCo.length) {
            var fMnbiD = MplMCo[HolCMn];
            HolCMn = HolCMn + 1;
            EgNgBG.dCLkjM.HolCMn = HolCMn;
            EgNgBG.jJNMeA(fMnbiD);
        } else {
            EgNgBG.AIIHhG.afPMfG();
        }
    };
    JpMdFf.prototype.cFaPCi = function () {
        if (!this.hBeflg) {
            return;
        };
        var DILNMg, MBllBn, MlomAd, hoMDEC;
        var hCHoIl = false;
        if (this.CnokOK.length > 0) {
            MlomAd = this.CnokOK.shift();
            hoMDEC = MlomAd[0];
            if (hoMDEC == 'i') {
                this.ImnNgj = MlomAd[1];
                this.AIIHhG.geEeHn();
                this.lMDGph([]);
                this.BkkBGK();
                this.ohHoOa = false;
                this.jaBFEF = [];
                hCHoIl = true;
                this.PnlGBG();
            } else if (hoMDEC == 's') {
                DILNMg = MlomAd[1].split(',');
                if (DILNMg.length == 2) {
                    MBllBn = NmbiKM(DILNMg[0]);
                    this.JCaDMM = BLAZE.nhjLnH.oAclpm('bitmap', 'checkers_figures_' + MBllBn);
                    this.dDfmCJ = 'chks_' + MBllBn + '_';
                    MBllBn = NmbiKM(DILNMg[1]);
                    this.CcHlaF = BLAZE.nhjLnH.oAclpm('bitmap', 'checkers_figures_' + MBllBn);
                    this.bLpagB = 'chks_' + MBllBn + '_';
                };
                if (this.ohHoOa) {
                    this.jhbgjk = MlomAd[2];
                } else {
                    this.fcNGMI(MlomAd[2]);
                }
            } else if (hoMDEC == 'a') {
                this.dNHMpc = NmbiKM(MlomAd[2]);
                this.mHLpEl = NmbiKM(MlomAd[1]);
                this.JnhGOm = false;
                this.kaLPng = 0;
                this.Npkhdf = 0;
                this.lMDGph([]);
                this.BkkBGK();
                this.CAKjCD = null;
                this.AIIHhG.gFepJD();
            } else if (hoMDEC == 'r') {
                this.JnhGOm = false;
                this.mHLpEl = 0;
                this.kaLPng = 0;
                this.Npkhdf = 0;
                this.lMDGph([]);
                this.BkkBGK();
                this.CAKjCD = null;
                this.AIIHhG.HamnNA();
            } else if (hoMDEC == 'p') {
                var HLiMHP = NmbiKM(MlomAd[1]);
                if ((this.eAeFAO.LcJlao != HLiMHP && HLiMHP > 0) || !this.eAeFAO.jHIGoB) {
                    this.dNHMpc = NmbiKM(MlomAd[3]);
                    this.PAdmoJ(NmbiKM(MlomAd[2]), MlomAd[4].split(':'));
                }
            } else {
                $warn('GC ' + hoMDEC);
            }
        };
        if (this.BidDIf.length > 0 && !hCHoIl) {
            this.AIIHhG.OgInlJ();
            var pKaopF = this.BidDIf.shift();
            var LeNpNP = HAELdp.OHokFB(knJbka() - pKaopF[0]);
            MlomAd = pKaopF[1];
            var bmfhpd = MlomAd.length;
            for (var fOGnCG = 0; fOGnCG < bmfhpd; fOGnCG++) {
                DILNMg = MlomAd[fOGnCG].split('#');
                hoMDEC = DILNMg[0];
                if (hoMDEC == 'p') {
                    if (DILNMg.length < 4) {
                        this.AIIHhG.MHIJhF(DILNMg[1], GbiMej('computer_player'), DILNMg[3]);
                    } else {
                        this.AIIHhG.MHIJhF(DILNMg[1], DILNMg[2], DILNMg[3]);
                    }
                } else if (hoMDEC == 's') {} else if (hoMDEC == 'i') {
                    this.AIIHhG.odcMgf(DILNMg[1], DILNMg[2]);
                } else if (hoMDEC == 'h') {
                    this.BlECiI(DILNMg[1], DILNMg[2]);
                } else if (hoMDEC == 'j') {
                    this.emfbLG(DILNMg[1], DILNMg[2]);
                } else if (hoMDEC == 'c') {
                    this.AIIHhG.haNiCk(DILNMg[1]);
                } else if (hoMDEC == 't') {
                    this.AIIHhG.CdFBij(NmbiKM(DILNMg[1]) + LeNpNP, DILNMg[2]);
                } else if (hoMDEC == 'e') {
                    this.AIIHhG.jBilmk(DILNMg[1]);
                } else if (hoMDEC == 'r') {
                    this.AIIHhG.FJEcfm(DILNMg[1], NmbiKM(DILNMg[2]) + LeNpNP);
                } else if (hoMDEC == 'w') {
                    this.AIIHhG.HjGcOh();
                    if (this.ohHoOa) {
                        this.PlMEmA = DILNMg;
                    } else {
                        this.JnhGOm = false;
                        this.mHLpEl = 0;
                        this.kaLPng = 0;
                        this.Npkhdf = 0;
                        this.lMDGph([]);
                        this.BkkBGK();
                        this.CAKjCD = null;
                        this.AIIHhG.HjGcOh();
                        this.AIIHhG.aBNniF(DILNMg[1], DILNMg[2], DILNMg[3], DILNMg[4], DILNMg[5], DILNMg[6]);
                        this.PlMEmA = null;
                    }
                } else if (hoMDEC == 'v') {
                    this.AIIHhG.gHDccP();
                    var FPNbFH = DILNMg.length;
                    for (var jGfFPE = 1; jGfFPE < FPNbFH; jGfFPE++) {
                        this.AIIHhG.MBnfai(DILNMg[jGfFPE]);
                    }
                } else if (hoMDEC == 'l') {
                    this.AIIHhG.MBnfai(DILNMg[1]);
                } else {
                    $warn('IC ' + hoMDEC);
                }
            };
        };
        if (this.CnokOK.length > 0 || this.BidDIf.length > 0) {
            this.cFaPCi();
        } else if (this.dCLkjM) {
            this.eopFHf();
        }
    };
    JpMdFf.prototype.jJNMeA = function (HLkCLj) {
        if (!this.hBeflg) {
            return;
        };
        if (!HLkCLj) {
            return;
        };
        if (HLkCLj.hasOwnProperty('gcn')) {
            this.AIIHhG.Ilmieb();
        };
        if (HLkCLj.hasOwnProperty('cpi')) {
            this.eAeFAO.LcJlao = NmbiKM(HLkCLj['cpi']);
        };
        var hKbcfc = false;
        if (HLkCLj.hasOwnProperty('gv')) {
            hKbcfc = true;
            var InIPKb = String(HLkCLj.gv).split('|');
            var bmfhpd = InIPKb.length;
            for (var fOGnCG = 0; fOGnCG < bmfhpd; fOGnCG++) {
                var AGbLFh = InIPKb[fOGnCG].split('#');
                var iMKLlL = AGbLFh[0];
                this.CnokOK.push(AGbLFh);
            }
        };
        if (HLkCLj.hasOwnProperty('gs')) {
            hKbcfc = true;
            this.BidDIf.push([knJbka(), String(HLkCLj.gs).split('|')]);
        };
        if (!this.cnaFhk && hKbcfc) {
            this.cFaPCi();
        }
    };
    JpMdFf.prototype.loNDBD = function (CGnGMk) {
        if (!this.hBeflg) {
            return;
        };
        this.fFMLbJ();
    };
    JpMdFf.prototype.iIKgJL = function (GmbBoJ, kcAcbf) {
        GmbBoJ = NmbiKM(GmbBoJ);
        kcAcbf = NmbiKM(kcAcbf);
        this.LlCjig = ejHLnG();
        this.AfePkf.nbpblG();
        this.LfjDoB = {};
        var McEjlk = this.LcdpGp.FeKiLh;
        McEjlk.table_default.style.backgroundImage = 'url("' + BLAZE.nhjLnH.oAclpm('bitmap', 'chess_default_table').src + '")';
        McEjlk.table_overlay.classList.remove('transition');
        McEjlk.table_overlay.style.backgroundImage = 'none';
        if (GmbBoJ > 0) {
            McEjlk.table_overlay.style.display = 'block';
            McEjlk.table_overlay.style.opacity = '0';
            var pKaopF = 'chb' + GmbBoJ;
            BLAZE.nhjLnH.dkgJMA(pKaopF, PMFAbI + pKaopF + '.png?' + BLAZE.CONTENT_VERSION, 1, this.kgEkDP, this);
        } else {
            McEjlk.table_overlay.style.display = 'none';
        }
    };
    JpMdFf.prototype.NKeAKN = function () {
        return (ejHLnG() - this.LlCjig) < 1000;
    };
    JpMdFf.prototype.kgEkDP = function (BiAKPf, aCKfgg, pMdaFp) {
        if (!pMdaFp || !aCKfgg) {
            return;
        };
        if (!pMdaFp.LcdpGp) {
            return;
        };
        var IgMlEF = pMdaFp.LcdpGp.FeKiLh.table_overlay;
        IgMlEF.style.backgroundImage = 'url("' + aCKfgg.src + '")';
        if (!pMdaFp.NKeAKN()) {
            IgMlEF.classList.add('transition');
        };
        IgMlEF.style.opacity = '1';
    };
    JpMdFf.prototype.fcNGMI = function (kOPkdE) {
        this.CAKjCD = null;
        this.jhbgjk = '';
        if (!this.hBeflg) {
            return;
        };
        if (!this.LcdpGp) {
            return;
        };
        var McEjlk = this.LcdpGp.FeKiLh;
        if (this.hCljaI != this.eAeFAO.LcJlao) {
            this.hCljaI = this.eAeFAO.LcJlao;
            if (this.hCljaI == 1 || this.hCljaI == 2) {
                McEjlk.table_base.classList.remove('FlipBoard');
                McEjlk.table_numbers.style.backgroundImage = 'url("' + BLAZE.nhjLnH.oAclpm('bitmap', 'chess_numbers_' + this.hCljaI).src + '")';
            } else {
                McEjlk.table_base.classList.add('FlipBoard');
                McEjlk.table_numbers.style.backgroundImage = 'url("' + BLAZE.nhjLnH.oAclpm('bitmap', 'chess_numbers_0').src + '")';
            };
            var DILNMg;
            var AFmnNn = McEjlk.table_sectors;
            for (var fOGnCG = 0; fOGnCG < 64; fOGnCG++) {
                var fMnbiD = McEjlk['s_' + fOGnCG];
                var pcDEfk = fOGnCG;
                var LFOfEg = pcDEfk % 8;
                var KLPIak = (pcDEfk - LFOfEg) / 8;
                if (this.hCljaI == 1) {
                    DILNMg = KLPIak;
                    KLPIak = LFOfEg;
                    LFOfEg = 7 - DILNMg;
                } else if (this.hCljaI == 2) {
                    DILNMg = KLPIak;
                    KLPIak = 7 - LFOfEg;
                    LFOfEg = DILNMg;
                };
                pcDEfk = KLPIak * 8 + LFOfEg;
                McEjlk['a_' + pcDEfk] = fMnbiD;
            }
        };
        this.lMDGph([]);
        this.BkkBGK();
        this.ohHoOa = false;
        this.jaBFEF = [];
        this.NgPjGI = {};
        var InIPKb = kOPkdE.split(';');
        var bmfhpd = InIPKb.length;
        for (var fOGnCG = 0; fOGnCG < bmfhpd; fOGnCG++) {
            var HIhniL = InIPKb[fOGnCG].split(':');
            if (HIhniL.length == 2) {
                this.NgPjGI['_' + NmbiKM(HIhniL[0])] = [NmbiKM(HIhniL[1]), 0];
            } else if (HIhniL.length == 3) {
                this.NgPjGI['_' + NmbiKM(HIhniL[0])] = [NmbiKM(HIhniL[1]), NmbiKM(HIhniL[2])];
            }
        };
        this.nOjkce();
        this.fmggND(1);
        this.fmggND(2);
    };
    JpMdFf.prototype.PnlGBG = function () {
        this.NgPjGI = {};
        this.nOjkce();
    };
    JpMdFf.prototype.nOjkce = function () {
        if (!this.hBeflg) {
            return;
        };
        if (!this.LcdpGp) {
            return;
        };
        if (this.hCljaI < 0) {
            return;
        };
        var APNChP;
        for (APNChP in this.NgPjGI) {
            var FhhdPP = NmbiKM(APNChP.substring(1));
            var lfhCNa = FhhdPP < 21;
            var IgMlEF = this.LfjDoB[APNChP];
            if (!IgMlEF) {
                if (lfhCNa) {
                    IgMlEF = new BLAZE.BKaEgK(this.JCaDMM, 1, 4, KJAHhc);
                    IgMlEF.igHPal = new BLAZE.BKaEgK(this.JCaDMM, 1, 4, KJAHhc);
                } else {
                    IgMlEF = new BLAZE.BKaEgK(this.CcHlaF, 1, 4, KJAHhc);
                    IgMlEF.igHPal = new BLAZE.BKaEgK(this.JCaDMM, 1, 4, KJAHhc);
                };
                IgMlEF.mcnbao(-1, IgMlEF.igHPal);
                this.AfePkf.mcnbao(-1, IgMlEF);
                this.LfjDoB[APNChP] = IgMlEF;
            };
            if (!lfhCNa) {
                if (this.NgPjGI[APNChP][1] > 0) {
                    IgMlEF.eHEgIc(3);
                    IgMlEF.igHPal.eHEgIc(5);
                } else {
                    IgMlEF.eHEgIc(1);
                    IgMlEF.igHPal.eHEgIc(4);
                }
            } else {
                if (this.NgPjGI[APNChP][1] > 0) {
                    IgMlEF.eHEgIc(2);
                    IgMlEF.igHPal.eHEgIc(5);
                } else {
                    IgMlEF.eHEgIc(0);
                    IgMlEF.igHPal.eHEgIc(4);
                }
            };
            lJELmO.cJJPaG(this.gNJJlP(this.NgPjGI[APNChP][0]), this.LfjDoB[APNChP].AcPOPM);
        };
        var mJeAlE = Object.keys(this.LfjDoB);
        var bmfhpd = mJeAlE.length;
        for (var fOGnCG = 0; fOGnCG < bmfhpd; fOGnCG++) {
            APNChP = mJeAlE[fOGnCG];
            if (!this.NgPjGI.hasOwnProperty(APNChP)) {
                this.AfePkf.anCblL(this.LfjDoB[APNChP]);
                delete this.LfjDoB[APNChP];
            }
        };
        this.AfePkf.aGcIfL();
    };
    JpMdFf.prototype.CGFGmI = function (AcPOPM) {
        var DILNMg;
        var LFOfEg = Math.round(Math.floor(AcPOPM[0] / nFhIkg));
        var KLPIak = Math.round(Math.floor(AcPOPM[1] / nFhIkg));
        if (this.hCljaI == 1) {
            DILNMg = KLPIak;
            KLPIak = LFOfEg;
            LFOfEg = 7 - DILNMg;
        } else if (this.hCljaI == 2) {
            DILNMg = KLPIak;
            KLPIak = 7 - LFOfEg;
            LFOfEg = DILNMg;
        };
        return [LFOfEg, KLPIak];
    };
    JpMdFf.prototype.MAgcCp = function (AcPOPM) {
        var DILNMg;
        var LFOfEg = Math.round(Math.floor(AcPOPM[0] / nFhIkg));
        var KLPIak = Math.round(Math.floor(AcPOPM[1] / nFhIkg));
        if (this.hCljaI == 1) {
            DILNMg = KLPIak;
            KLPIak = LFOfEg;
            LFOfEg = 7 - DILNMg;
        } else if (this.hCljaI == 2) {
            DILNMg = KLPIak;
            KLPIak = 7 - LFOfEg;
            LFOfEg = DILNMg;
        };
        return Math.round(LFOfEg + (KLPIak * 8));
    };
    JpMdFf.prototype.bNNnfJ = function (pcDEfk) {
        var LFOfEg = pcDEfk % 8;
        var KLPIak = (pcDEfk - LFOfEg) / 8;
        return [LFOfEg, KLPIak];
    };
    JpMdFf.prototype.gNJJlP = function (pcDEfk) {
        var DILNMg;
        var LFOfEg = pcDEfk % 8;
        var KLPIak = (pcDEfk - LFOfEg) / 8;
        if (this.hCljaI == 1) {
            DILNMg = KLPIak;
            KLPIak = 7 - LFOfEg;
            LFOfEg = DILNMg;
        } else if (this.hCljaI == 2) {
            DILNMg = KLPIak;
            KLPIak = LFOfEg;
            LFOfEg = 7 - DILNMg;
        };
        return [(LFOfEg * nFhIkg) + OmPPLi[0], (KLPIak * nFhIkg) + OmPPLi[1]];
    };
    JpMdFf.prototype.IlaoKI = function (pcDEfk) {
        var LFOfEg = pcDEfk % 8;
        var KLPIak = (pcDEfk - LFOfEg) / 8;
        if (KLPIak % 2 == 0) {
            return LFOfEg % 2 != 0;
        } else {
            return LFOfEg % 2 == 0;
        }
    };
    JpMdFf.prototype.BlECiI = function (dKglFf, MlomAd) {
        if (!this.LcdpGp) {
            return;
        };
        if (dKglFf != 1 && dKglFf != 2) {
            return;
        };
        this.CaPgMf['_' + dKglFf] = [];
        this.emfbLG(dKglFf, MlomAd);
    };
    JpMdFf.prototype.emfbLG = function (dKglFf, MlomAd) {
        if (!this.LcdpGp) {
            return;
        };
        if (dKglFf != 1 && dKglFf != 2) {
            return;
        };
        var JlbiDa = this.CaPgMf['_' + dKglFf];
        var HIhniL = MlomAd.split(':');
        var bmfhpd = HIhniL.length;
        for (var fOGnCG = 0; fOGnCG < bmfhpd; fOGnCG++) {
            var DILNMg = HIhniL[fOGnCG].split('.');
            if (DILNMg.length == 2) {
                JlbiDa.push([NmbiKM(DILNMg[0]), NmbiKM(DILNMg[1])]);
            }
        };
        this.fmggND(dKglFf);
    };
    JpMdFf.prototype.fmggND = function (dKglFf) {
        if (!this.LcdpGp) {
            return;
        };
        if (!this.JCaDMM || !this.CcHlaF) {
            return;
        };
        var Biabka;
        var ljCiCc = '';
        if (this.hCljaI == 1) {
            if (dKglFf == 1) {
                ljCiCc = 'url("' + this.CcHlaF.src + '")';
                Biabka = this.LcdpGp.FeKiLh['stack_1'];
            } else if (dKglFf == 2) {
                ljCiCc = 'url("' + this.JCaDMM.src + '")';
                Biabka = this.LcdpGp.FeKiLh['stack_2'];
            } else {
                return;
            }
        } else if (this.hCljaI == 2) {
            if (dKglFf == 1) {
                ljCiCc = 'url("' + this.CcHlaF.src + '")';
                Biabka = this.LcdpGp.FeKiLh['stack_2'];
            } else if (dKglFf == 2) {
                ljCiCc = 'url("' + this.JCaDMM.src + '")';
                Biabka = this.LcdpGp.FeKiLh['stack_1'];
            } else {
                return;
            }
        } else {
            if (dKglFf == 1) {
                ljCiCc = 'url("' + this.CcHlaF.src + '")';
                Biabka = this.LcdpGp.FeKiLh['stack_2'];
            } else if (dKglFf == 2) {
                ljCiCc = 'url("' + this.JCaDMM.src + '")';
                Biabka = this.LcdpGp.FeKiLh['stack_1'];
            } else {
                return;
            }
        };
        var JlbiDa = this.CaPgMf['_' + dKglFf];
        var IgMlEF, bmfhpd = JlbiDa.length;
        for (var fOGnCG = 0; fOGnCG < HOCLcO; fOGnCG++) {
            var jaNIpg = 'S' + fOGnCG;
            var GCmDhM = 'E' + fOGnCG;
            if (fOGnCG >= bmfhpd) {
                IgMlEF = Biabka[GCmDhM];
                if (IgMlEF) {
                    if (IgMlEF.parentNode) {
                        IgMlEF.parentNode.removeChild(IgMlEF);
                    };
                    IgMlEF = null;
                    delete Biabka[GCmDhM];
                };
                IgMlEF = Biabka[jaNIpg];
                if (IgMlEF) {
                    if (IgMlEF.parentNode) {
                        IgMlEF.parentNode.removeChild(IgMlEF);
                    };
                    IgMlEF = null;
                    delete Biabka[jaNIpg];
                }
            } else {
                var DILNMg = JlbiDa[fOGnCG];
                var lfhCNa = DILNMg[0] < 21;
                var difnaM = DILNMg[1] > 0;
                IgMlEF = Biabka[jaNIpg];
                if (!IgMlEF) {
                    IgMlEF = document.createElement('div');
                    Biabka[jaNIpg] = IgMlEF;
                    Biabka.appendChild(IgMlEF);
                };
                IgMlEF.style.backgroundImage = ljCiCc;
                if (difnaM) {
                    IgMlEF.className = 'CheckerShadow Frame5';
                } else {
                    IgMlEF.className = 'CheckerShadow Frame4';
                };
                IgMlEF = Biabka[GCmDhM];
                if (!IgMlEF) {
                    IgMlEF = document.createElement('div');
                    Biabka[GCmDhM] = IgMlEF;
                    Biabka[jaNIpg].appendChild(IgMlEF);
                };
                IgMlEF.style.backgroundImage = ljCiCc;
                if (lfhCNa) {
                    if (difnaM) {
                        IgMlEF.className = 'CheckerFigure Frame2';
                    } else {
                        IgMlEF.className = 'CheckerFigure Frame0';
                    }
                } else {
                    if (difnaM) {
                        IgMlEF.className = 'CheckerFigure Frame3';
                    } else {
                        IgMlEF.className = 'CheckerFigure Frame1';
                    }
                };
            }
        };
    };
    JpMdFf.prototype.JDaDFO = function (pcDEfk) {
        if (!this.LcdpGp || !this.MglooE) {
            return;
        };
        this.BkkBGK();
        if (this.MglooE.parentNode) {
            this.MglooE.parentNode.removeChild(this.MglooE);
        };
        this.MglooE.classList.remove('Transition');
        this.MglooE.style.opacity = 1;
        var McEjlk = this.LcdpGp.FeKiLh;
        var hJBOIC = 'a_' + pcDEfk;
        if (!McEjlk[hJBOIC]) {
            return;
        };
        McEjlk[hJBOIC].appendChild(this.MglooE);
    };
    JpMdFf.prototype.BkkBGK = function () {
        if (this.MglooE) {
            this.MglooE.classList.add('Transition');
            this.MglooE.style.opacity = 0;
        }
    };
    JpMdFf.prototype.fhKaMP = function (pcDEfk) {
        if (!this.LcdpGp || !this.npicEG) {
            return;
        };
        if (this.npicEG.parentNode) {
            this.npicEG.parentNode.removeChild(this.npicEG);
        };
        var McEjlk = this.LcdpGp.FeKiLh;
        var hJBOIC = 'a_' + pcDEfk;
        if (!McEjlk[hJBOIC]) {
            return;
        };
        McEjlk[hJBOIC].appendChild(this.npicEG);
        this.npicEG.style.display = 'none';
        this.npicEG.classList.remove('Animation');
        this.npicEG.style.display = '';
        this.npicEG.classList.add('Animation');
    };
    JpMdFf.prototype.lMDGph = function (AFmnNn) {
        if (!this.LcdpGp) {
            return;
        };
        var McEjlk = this.LcdpGp.FeKiLh;
        var NcdPLc = {};
        var fOGnCG, bmfhpd = AFmnNn.length;
        for (fOGnCG = 0; fOGnCG < bmfhpd; fOGnCG++) {
            NcdPLc['_' + AFmnNn[fOGnCG]] = true;
        };
        for (fOGnCG = 0; fOGnCG < 64; fOGnCG++) {
            var fMnbiD = McEjlk['a_' + fOGnCG];
            if (fMnbiD) {
                if (NcdPLc['_' + fOGnCG]) {
                    if (this.IlaoKI(fOGnCG)) {
                        fMnbiD.classList.add('CH_White');
                    } else {
                        fMnbiD.classList.add('CH_Black');
                    }
                } else {
                    fMnbiD.classList.remove('CH_Black');
                    fMnbiD.classList.remove('CH_White');
                }
            };
        }
    };
    JpMdFf.prototype.PAdmoJ = function (FhhdPP, cfagom) {
        if (!cfagom) {
            return;
        };
        if (!this.hBeflg) {
            return;
        };
        var khkhcP = [];
        var bmfhpd = cfagom.length;
        for (var fOGnCG = 0; fOGnCG < bmfhpd; fOGnCG++) {
            khkhcP.push([FhhdPP, NmbiKM(cfagom[fOGnCG])]);
        };
        this.dfEdDm(khkhcP);
    };
    JpMdFf.prototype.dfEdDm = function (khkhcP) {
        if (!khkhcP) {
            return;
        };
        if (!this.hBeflg) {
            return;
        };
        if (this.ohHoOa) {
            var bmfhpd = this.jaBFEF.length;
            for (var fOGnCG = 0; fOGnCG < bmfhpd; fOGnCG++) {
                var fCmCdh = this.jaBFEF[fOGnCG];
                var APNChP = '_' + fCmCdh[0];
                var pBOFOj = NmbiKM(fCmCdh[1]) % 64;
                if (this.LfjDoB[APNChP]) {
                    this.LfjDoB[APNChP].AcPOPM = this.gNJJlP(pBOFOj);
                }
            };
            this.AfePkf.aGcIfL();
        };
        this.ohHoOa = true;
        this.jaBFEF = khkhcP;
        this.IFnEGf();
    };
    JpMdFf.prototype.IFnEGf = function () {
        if (!this.hBeflg || !this.ohHoOa) {
            return;
        };
        var HHNLkp;
        if (this.BiiEId != '') {
            if (this.LfjDoB[this.BiiEId]) {
                this.AfePkf.anCblL(this.LfjDoB[this.BiiEId]);
                delete this.LfjDoB[this.BiiEId];
            };
            this.BiiEId = '';
        };
        if (this.jjDfaE > 20) {
            HHNLkp = this.bLpagB;
        } else {
            HHNLkp = this.dDfmCJ;
        };
        if (this.jjDfaE > 0) {
            if (this.OiilAB) {
                JMBDGp.gDicAB(HHNLkp + 'hit', 1, false, 0, true);
            }
        };
        if (this.jaBFEF.length < 1) {
            if (this.jjDfaE >= 0 && this.kJGCli && !this.JnhGOm) {
                var nofkKK = '_' + this.jjDfaE;
                if (this.NgPjGI[nofkKK]) {
                    if (this.NgPjGI[nofkKK][1] == 0) {
                        var cMNfpi = this.bNNnfJ(this.joEnMj);
                        var hmFbMC = -1;
                        if (this.jjDfaE < 21) {
                            if (cMNfpi[0] == 7) {
                                hmFbMC = 2;
                            }
                        } else {
                            if (cMNfpi[0] == 0) {
                                hmFbMC = 3;
                            }
                        };
                        if (hmFbMC >= 0) {
                            JMBDGp.gDicAB(HHNLkp + 'crowned', 1, false, 0, true);
                            this.kJGCli.eHEgIc(hmFbMC);
                        }
                    };
                }
            };
            if (this.kJGCli) {
                this.kJGCli.igHPal.HilidP = true;
                this.kJGCli = null;
            };
            this.jjDfaE = -1;
            this.ohHoOa = false;
            if (this.jhbgjk != '') {
                this.fcNGMI(this.jhbgjk);
            } else {
                this.AfePkf.aGcIfL();
            };
            if (this.JnhGOm) {
                if (this.lfbBml) {
                    if (this.mJEfnh) {
                        this.lMDGph(this.lfbBml.AFmnNn);
                    }
                };
            };
            if (this.PlMEmA) {
                this.JnhGOm = false;
                this.mHLpEl = 0;
                this.kaLPng = 0;
                this.Npkhdf = 0;
                this.lMDGph([]);
                this.BkkBGK();
                this.CAKjCD = null;
                this.AIIHhG.HjGcOh();
                this.AIIHhG.aBNniF(this.PlMEmA[1], this.PlMEmA[2], this.PlMEmA[3], this.PlMEmA[4], this.PlMEmA[5], this.PlMEmA[6]);
                this.PlMEmA = null;
            };
            if (this.dCLkjM) {
                this.eopFHf();
            }
        } else {
            var fCmCdh = this.jaBFEF.shift();
            var APNChP = '_' + fCmCdh[0];
            var pBOFOj = NmbiKM(fCmCdh[1]) % 64;
            if (this.LfjDoB[APNChP]) {
                if (!this.JnhGOm) {
                    this.fhKaMP(pBOFOj);
                };
                this.ohHoOa = true;
                this.jjDfaE = fCmCdh[0];
                this.BiiEId = '';
                this.kJGCli = this.LfjDoB[APNChP];
                this.joEnMj = pBOFOj;
                this.JOCPJN = this.gNJJlP(pBOFOj);
                this.MJEPlf = lJELmO.NoeNdn(this.kJGCli.AcPOPM);
                this.LgPhAh = lJELmO.khOMcp(this.JOCPJN, this.MJEPlf);
                this.kFlNgO = lJELmO.PaaKha(this.LgPhAh);
                this.POBAKo = this.kFlNgO * 0.5;
                this.IkOPfg = 1 / this.POBAKo / this.POBAKo;
                this.hlMcjF = 0;
                this.GmcLeF = 0;
                this.OiilAB = this.kFlNgO / nFhIkg > 1.9;
                if (this.OiilAB) {
                    this.EiIkmG = ifKjBF;
                } else {
                    this.EiIkmG = pajMJA;
                };
                if (this.OiilAB) {
                    var fOGnCG, dgLdGd;
                    var cfiLMN = {};
                    for (var kdbnIl in this.NgPjGI) {
                        cfiLMN['_' + this.NgPjGI[kdbnIl][0]] = kdbnIl;
                    };
                    var dkFCBH = '';
                    var hENPHg = this.CGFGmI(this.MJEPlf);
                    var EKmDDK = this.bNNnfJ(pBOFOj);
                    if (EKmDDK[0] > hENPHg[0]) {
                        if (EKmDDK[1] > hENPHg[1]) {
                            for (fOGnCG = 0; fOGnCG < 7; fOGnCG++) {
                                hENPHg[0] = hENPHg[0] + 1;
                                hENPHg[1] = hENPHg[1] + 1;
                                if (hENPHg[0] >= EKmDDK[0] && hENPHg[1] >= EKmDDK[1]) {
                                    break;
                                };
                                dgLdGd = '_' + Math.round(hENPHg[0] + (hENPHg[1] * 8));
                                if (cfiLMN[dgLdGd]) {
                                    this.BiiEId = cfiLMN[dgLdGd];
                                    break;
                                }
                            };
                        } else {
                            for (fOGnCG = 0; fOGnCG < 7; fOGnCG++) {
                                hENPHg[0] = hENPHg[0] + 1;
                                hENPHg[1] = hENPHg[1] - 1;
                                if (hENPHg[0] >= EKmDDK[0] && hENPHg[1] <= EKmDDK[1]) {
                                    break;
                                };
                                dgLdGd = '_' + Math.round(hENPHg[0] + (hENPHg[1] * 8));
                                if (cfiLMN[dgLdGd]) {
                                    this.BiiEId = cfiLMN[dgLdGd];
                                    break;
                                }
                            };
                        }
                    } else {
                        if (EKmDDK[1] > hENPHg[1]) {
                            for (fOGnCG = 0; fOGnCG < 7; fOGnCG++) {
                                hENPHg[0] = hENPHg[0] - 1;
                                hENPHg[1] = hENPHg[1] + 1;
                                if (hENPHg[0] <= EKmDDK[0] && hENPHg[1] >= EKmDDK[1]) {
                                    break;
                                };
                                dgLdGd = '_' + Math.round(hENPHg[0] + (hENPHg[1] * 8));
                                if (cfiLMN[dgLdGd]) {
                                    this.BiiEId = cfiLMN[dgLdGd];
                                    break;
                                }
                            };
                        } else {
                            for (fOGnCG = 0; fOGnCG < 7; fOGnCG++) {
                                hENPHg[0] = hENPHg[0] - 1;
                                hENPHg[1] = hENPHg[1] - 1;
                                if (hENPHg[0] <= EKmDDK[0] && hENPHg[1] <= EKmDDK[1]) {
                                    break;
                                };
                                dgLdGd = '_' + Math.round(hENPHg[0] + (hENPHg[1] * 8));
                                if (cfiLMN[dgLdGd]) {
                                    this.BiiEId = cfiLMN[dgLdGd];
                                    break;
                                }
                            };
                        }
                    };
                    if (this.BiiEId == '') {
                        this.OiilAB = false;
                    }
                };
                if (this.jjDfaE > 20) {
                    HHNLkp = this.bLpagB;
                } else {
                    HHNLkp = this.dDfmCJ;
                };
                this.AfePkf.LfFMlG(this.kJGCli);
                if (this.OiilAB) {
                    this.kJGCli.igHPal.HilidP = false;
                } else {
                    this.kJGCli.igHPal.HilidP = true;
                    JMBDGp.gDicAB(HHNLkp + 'move', 1, false, 0, true);
                };
                if (this.BiiEId != '') {
                    var MKjgcC = NmbiKM(this.BiiEId.substring(1));
                    if (MKjgcC < 21) {
                        HHNLkp = this.bLpagB;
                    } else {
                        HHNLkp = this.dDfmCJ;
                    };
                    JMBDGp.gDicAB(HHNLkp + 'kill', 1, false, 0, true);
                }
            } else {
                this.IFnEGf();
            }
        };
    };
    JpMdFf.prototype.fFMLbJ = function () {
        if (!this.ohHoOa) {
            return;
        };
        if (this.kJGCli) {
            this.hlMcjF = this.hlMcjF + BLAZE.paIPdi.KeOOoA;
            if (this.hlMcjF < this.EiIkmG) {
                this.GmcLeF = (this.hlMcjF / this.EiIkmG) * this.kFlNgO;
                var akdcAH = lJELmO.PAGKnH(this.LgPhAh, this.GmcLeF / this.kFlNgO);
                lJELmO.jeDgdF(akdcAH, this.MJEPlf);
                if (this.OiilAB) {
                    var EhoLJF = Math.abs(this.GmcLeF - this.POBAKo);
                    EhoLJF = kBLkHE - (kBLkHE * EhoLJF * EhoLJF * this.IkOPfg);
                    akdcAH[1] = akdcAH[1] - EhoLJF;
                };
                this.kJGCli.AcPOPM = akdcAH;
                this.AfePkf.aGcIfL();
                return;
            };
            this.kJGCli.AcPOPM = this.JOCPJN;
        };
        this.IFnEGf();
        this.AfePkf.aGcIfL();
    };
    JpMdFf.prototype.JnNiaM = function (EAmjJJ) {
        var IgMlEF = EAmjJJ.target;
        if (EAmjJJ.type == 'touchend') {
            if (EAmjJJ.changedTouches.length < 1) {
                return;
            };
            var lboAhk = EAmjJJ.changedTouches[0];
            EAmjJJ.preventDefault();
            EAmjJJ.stopPropagation();
            IgMlEF = document.elementFromPoint(lboAhk.clientX, lboAhk.clientY);
        } else if (EAmjJJ.type == 'touchstart') {
            EAmjJJ.preventDefault();
            EAmjJJ.stopPropagation();
        };
        if (!IgMlEF) {
            return;
        };
        if (!IgMlEF.parentNode) {
            return;
        };
        if (!IgMlEF.parentNode.imODiM) {
            return;
        };
        IgMlEF.parentNode.imODiM.oJfEFP(EAmjJJ.type, IgMlEF.pcDEfk);
    };
    JpMdFf.prototype.oJfEFP = function (dFlGoB, pcDEfk) {
        if (this.dCLkjM) {
            this.oODIpi();
            return;
        };
        if (!this.hBeflg || !this.eAeFAO.jHIGoB || this.ohHoOa || this.mHLpEl < 1) {
            return;
        };
        pcDEfk = NmbiKM(pcDEfk);
        var DILNMg, HHNLkp;
        var LFOfEg = pcDEfk % 8;
        var KLPIak = (pcDEfk - LFOfEg) / 8;
        if (this.hCljaI == 1) {
            DILNMg = KLPIak;
            KLPIak = LFOfEg;
            LFOfEg = 7 - DILNMg;
        } else if (this.hCljaI == 2) {
            DILNMg = KLPIak;
            KLPIak = 7 - LFOfEg;
            LFOfEg = DILNMg;
        };
        pcDEfk = KLPIak * 8 + LFOfEg;
        if (this.IlaoKI(pcDEfk)) {
            return;
        };
        var FhhdPP = 0;
        for (var APNChP in this.NgPjGI) {
            if (this.NgPjGI[APNChP][0] == pcDEfk) {
                FhhdPP = NmbiKM(APNChP.substring(1));
                break;
            }
        };
        this.bIJNNo(this.mHLpEl, false);
        if (this.kaLPng == 0) {
            if (dFlGoB == 'mousedown' || dFlGoB == 'touchstart') {
                if (FhhdPP > 0) {
                    if (this.mHLpEl == 1) {
                        if (FhhdPP > 20) {
                            return;
                        };
                        HHNLkp = this.dDfmCJ;
                    } else if (this.mHLpEl == 2) {
                        if (FhhdPP < 21) {
                            return;
                        };
                        HHNLkp = this.bLpagB;
                    } else {
                        return;
                    };
                    JMBDGp.gDicAB(HHNLkp + 'click', 1, false, 0, true);
                    this.MAnAPL = [];
                    this.kaLPng = FhhdPP;
                    this.Npkhdf = pcDEfk;
                    this.JDaDFO(pcDEfk);
                    this.lfbBml = this.PaNDGP(this.kaLPng);
                    if (this.mJEfnh) {
                        this.lMDGph(this.lfbBml.AFmnNn);
                    }
                };
            }
        } else {
            if (dFlGoB == 'mousedown' || dFlGoB == 'touchstart') {
                if (!this.JnhGOm) {
                    if (this.kaLPng == FhhdPP || this.Npkhdf == pcDEfk) {} else {
                        if (FhhdPP > 0) {
                            if (this.mHLpEl == 1) {
                                if (FhhdPP > 20) {
                                    return;
                                };
                                HHNLkp = this.dDfmCJ;
                            } else if (this.mHLpEl == 2) {
                                if (FhhdPP < 21) {
                                    return;
                                };
                                HHNLkp = this.bLpagB;
                            } else {
                                return;
                            };
                            this.MAnAPL = [];
                            this.kaLPng = FhhdPP;
                            this.Npkhdf = pcDEfk;
                            this.JDaDFO(pcDEfk);
                            this.lfbBml = this.PaNDGP(this.kaLPng);
                            if (this.mJEfnh) {
                                this.lMDGph(this.lfbBml.AFmnNn);
                            };
                            JMBDGp.gDicAB(HHNLkp + 'click', 1, false, 0, true);
                        }
                    };
                }
            } else if (dFlGoB == 'mouseup' || dFlGoB == 'touchend') {
                if (FhhdPP == 0) {
                    if (this.lfbBml) {
                        var HbnLBg = '_' + pcDEfk;
                        if (this.lfbBml.hasOwnProperty(HbnLBg)) {
                            this.MAnAPL.push(pcDEfk);
                            this.lMDGph([]);
                            this.dfEdDm([[this.kaLPng, pcDEfk]]);
                            var fpMgcJ = this.lfbBml[HbnLBg];
                            var aPpFJd = false;
                            if (fpMgcJ > 0) {
                                fpMgcJ = '_' + fpMgcJ;
                                if (this.NgPjGI[fpMgcJ]) {
                                    delete this.NgPjGI[fpMgcJ];
                                }
                            } else {
                                aPpFJd = true;
                            };
                            this.NgPjGI['_' + this.kaLPng][0] = pcDEfk;
                            if (!aPpFJd) {
                                if (this.BJoBNk[1] == 'amcheckers') {
                                    if (this.NgPjGI['_' + this.kaLPng][1] == 0) {
                                        var PHdOPo = this.bNNnfJ(pcDEfk);
                                        if (this.mHLpEl == 1) {
                                            aPpFJd = PHdOPo[0] == 7;
                                        } else {
                                            aPpFJd = PHdOPo[0] == 0;
                                        }
                                    };
                                }
                            };
                            if (!aPpFJd) {
                                this.CAKjCD = null;
                                this.bIJNNo(this.mHLpEl, true);
                                this.lfbBml = this.PaNDGP(this.kaLPng);
                                if (this.lfbBml.AFmnNn.length > 0 && this.lfbBml.fpMgcJ) {
                                    this.JnhGOm = true;
                                    this.JDaDFO(pcDEfk);
                                    return;
                                }
                            };
                            this.lfbBml = null;
                            this.CAKjCD = null;
                            this.mHLpEl = 0;
                            this.BkkBGK();
                            this.AIIHhG.DJMNpK({
                                c: 'move',
                                v: this.kaLPng + ':' + this.MAnAPL.join(':')
                            });
                            this.MAnAPL = [];
                            this.AIIHhG.HamnNA();
                        }
                    };
                }
            };
        }
    };
    JpMdFf.prototype.PaNDGP = function (FhhdPP) {
        if (this.CAKjCD) {
            var APNChP = '_' + FhhdPP;
            if (this.CAKjCD[APNChP]) {
                return this.CAKjCD[APNChP];
            }
        };
        return {
            AFmnNn: [],
            fpMgcJ: false
        };
    };
    JpMdFf.prototype.bIJNNo = function (kIKhFD, DahAEb) {
        if (this.CAKjCD) {
            return;
        };
        this.CAKjCD = {};
        var fOGnCG, bmfhpd, APNChP, FhhdPP;
        var IBpkAb = [];
        var cfiLMN = {};
        for (APNChP in this.NgPjGI) {
            FhhdPP = NmbiKM(APNChP.substring(1));
            cfiLMN['_' + this.NgPjGI[APNChP][0]] = FhhdPP;
            if (kIKhFD == 1) {
                if (FhhdPP < 21) {
                    IBpkAb.push(FhhdPP);
                }
            } else {
                if (FhhdPP > 20) {
                    IBpkAb.push(FhhdPP);
                }
            };
        };
        var pipbLm = false;
        bmfhpd = IBpkAb.length;
        for (fOGnCG = 0; fOGnCG < bmfhpd; fOGnCG++) {
            FhhdPP = IBpkAb[fOGnCG];
            APNChP = '_' + FhhdPP;
            this.CAKjCD[APNChP] = this.dkGAAH(FhhdPP, cfiLMN, DahAEb);
            if (this.CAKjCD[APNChP].fpMgcJ) {
                pipbLm = true;
            }
        };
        if (pipbLm) {
            for (APNChP in this.CAKjCD) {
                var fCmCdh = this.CAKjCD[APNChP];
                if (!fCmCdh.fpMgcJ) {
                    if (fCmCdh.AFmnNn.length > 0) {
                        this.CAKjCD[APNChP] = {
                            AFmnNn: [],
                            fpMgcJ: false
                        };
                    }
                };
            }
        };
    };
    JpMdFf.prototype.dkGAAH = function (FhhdPP, cfiLMN, DahAEb) {
        var fOGnCG, bmfhpd, kdbnIl, dgLdGd, lGjFpn, IOOgda, iCpknH, APNChP, llIIgc, EhoLJF, aFmigA;
        var KmngMC = this.BJoBNk[1];
        var khkhcP = {
            AFmnNn: [],
            fpMgcJ: false
        };
        APNChP = '_' + FhhdPP;
        if (!this.NgPjGI[APNChP]) {
            return;
        };
        var NdlloI = this.NgPjGI[APNChP][0];
        var hENPHg = this.bNNnfJ(NdlloI);
        var difnaM = this.NgPjGI[APNChP][1] > 0;
        var lfhCNa = FhhdPP < 21;
        var jBFdkl, paEjmJ;
        if (KmngMC == 'gzcheckers' || KmngMC == 'anticheckers') {
            if (difnaM) {
                this.PjeOla([-1, -1], lfhCNa, hENPHg, khkhcP, cfiLMN, false);
                this.PjeOla([-1, 1], lfhCNa, hENPHg, khkhcP, cfiLMN, false);
                this.PjeOla([1, -1], lfhCNa, hENPHg, khkhcP, cfiLMN, false);
                this.PjeOla([1, 1], lfhCNa, hENPHg, khkhcP, cfiLMN, false);
                if (khkhcP.fpMgcJ) {
                    var MOMKii = {
                        AFmnNn: [],
                        fpMgcJ: true
                    };
                    for (kdbnIl in khkhcP) {
                        if (kdbnIl.substring(0, 1) == '_') {
                            if (khkhcP[kdbnIl] > 0) {
                                MOMKii[kdbnIl] = khkhcP[kdbnIl];
                                MOMKii.AFmnNn.push(NmbiKM(kdbnIl.substring(1)));
                            }
                        };
                    };
                    khkhcP = MOMKii;
                }
            } else {
                jBFdkl = [[1, -1], [1, 1]];
                paEjmJ = [[2, -2, -7], [2, 2, 9], [-2, -2, -9], [-2, 2, 7]];
                bmfhpd = paEjmJ.length;
                for (fOGnCG = 0; fOGnCG < bmfhpd; fOGnCG++) {
                    EhoLJF = paEjmJ[fOGnCG];
                    if (lfhCNa) {
                        iCpknH = NdlloI + EhoLJF[2];
                    } else {
                        lJELmO.ibGKip(EhoLJF);
                        iCpknH = NdlloI - EhoLJF[2];
                    };
                    llIIgc = lJELmO.mCMKjO(hENPHg, EhoLJF);
                    if (llIIgc[0] < 0 || llIIgc[0] > 7) {
                        continue;
                    };
                    if (llIIgc[1] < 0 || llIIgc[1] > 7) {
                        continue;
                    };
                    lGjFpn = llIIgc[1] * 8 + llIIgc[0];
                    dgLdGd = '_' + lGjFpn;
                    IOOgda = '_' + iCpknH;
                    if (!cfiLMN.hasOwnProperty(dgLdGd)) {
                        if (cfiLMN.hasOwnProperty(IOOgda)) {
                            kdbnIl = cfiLMN[IOOgda];
                            if (lfhCNa) {
                                if (kdbnIl < 21) {
                                    continue;
                                }
                            } else {
                                if (kdbnIl > 20) {
                                    continue;
                                }
                            };
                            khkhcP.fpMgcJ = true;
                            khkhcP[dgLdGd] = kdbnIl;
                            khkhcP.AFmnNn.push(lGjFpn);
                        }
                    };
                };
                if (!khkhcP.fpMgcJ) {
                    bmfhpd = jBFdkl.length;
                    for (fOGnCG = 0; fOGnCG < bmfhpd; fOGnCG++) {
                        EhoLJF = jBFdkl[fOGnCG];
                        if (!lfhCNa) {
                            lJELmO.ibGKip(EhoLJF);
                        };
                        llIIgc = lJELmO.mCMKjO(hENPHg, EhoLJF);
                        if (llIIgc[0] < 0 || llIIgc[0] > 7) {
                            continue;
                        };
                        if (llIIgc[1] < 0 || llIIgc[1] > 7) {
                            continue;
                        };
                        lGjFpn = llIIgc[1] * 8 + llIIgc[0];
                        dgLdGd = '_' + lGjFpn;
                        if (!cfiLMN.hasOwnProperty(dgLdGd)) {
                            khkhcP[dgLdGd] = 0;
                            khkhcP.AFmnNn.push(lGjFpn);
                        }
                    };
                }
            };
        } else if (KmngMC == 'amcheckers') {
            if (difnaM) {
                jBFdkl = [[1, -1], [1, 1], [-1, 1], [-1, -1]];
                paEjmJ = [[2, -2, -7], [2, 2, 9], [-2, -2, -9], [-2, 2, 7]];
            } else {
                jBFdkl = [[1, -1], [1, 1]];
                if (DahAEb) {
                    paEjmJ = [[2, -2, -7], [2, 2, 9], [-2, -2, -9], [-2, 2, 7]];
                } else {
                    paEjmJ = [[2, -2, -7], [2, 2, 9]];
                }
            };
            bmfhpd = paEjmJ.length;
            for (fOGnCG = 0; fOGnCG < bmfhpd; fOGnCG++) {
                EhoLJF = paEjmJ[fOGnCG];
                if (lfhCNa) {
                    iCpknH = NdlloI + EhoLJF[2];
                } else {
                    lJELmO.ibGKip(EhoLJF);
                    iCpknH = NdlloI - EhoLJF[2];
                };
                llIIgc = lJELmO.mCMKjO(hENPHg, EhoLJF);
                if (llIIgc[0] < 0 || llIIgc[0] > 7) {
                    continue;
                };
                if (llIIgc[1] < 0 || llIIgc[1] > 7) {
                    continue;
                };
                lGjFpn = llIIgc[1] * 8 + llIIgc[0];
                dgLdGd = '_' + lGjFpn;
                IOOgda = '_' + iCpknH;
                if (!cfiLMN.hasOwnProperty(dgLdGd)) {
                    if (cfiLMN.hasOwnProperty(IOOgda)) {
                        kdbnIl = cfiLMN[IOOgda];
                        if (lfhCNa) {
                            if (kdbnIl < 21) {
                                continue;
                            }
                        } else {
                            if (kdbnIl > 20) {
                                continue;
                            }
                        };
                        khkhcP.fpMgcJ = true;
                        khkhcP[dgLdGd] = kdbnIl;
                        khkhcP.AFmnNn.push(lGjFpn);
                    }
                };
            };
            if (!khkhcP.fpMgcJ) {
                bmfhpd = jBFdkl.length;
                for (fOGnCG = 0; fOGnCG < bmfhpd; fOGnCG++) {
                    EhoLJF = jBFdkl[fOGnCG];
                    if (!lfhCNa) {
                        lJELmO.ibGKip(EhoLJF);
                    };
                    llIIgc = lJELmO.mCMKjO(hENPHg, EhoLJF);
                    if (llIIgc[0] < 0 || llIIgc[0] > 7) {
                        continue;
                    };
                    if (llIIgc[1] < 0 || llIIgc[1] > 7) {
                        continue;
                    };
                    lGjFpn = llIIgc[1] * 8 + llIIgc[0];
                    dgLdGd = '_' + lGjFpn;
                    if (!cfiLMN.hasOwnProperty(dgLdGd)) {
                        khkhcP[dgLdGd] = 0;
                        khkhcP.AFmnNn.push(lGjFpn);
                    }
                };
            }
        };
        return khkhcP;
    };
    JpMdFf.prototype.PjeOla = function (EhoLJF, lfhCNa, hENPHg, khkhcP, cfiLMN, NPicpE) {
        var lcmkjE = {};
        var CPagiO = [];
        var aFmigA = 0;
        var fOGnCG, bmfhpd, kdbnIl, mJeAlE, lGjFpn, dgLdGd, PHdOPo = lJELmO.NoeNdn(hENPHg);
        for (fOGnCG = 0; fOGnCG < 7; fOGnCG++) {
            lJELmO.jeDgdF(PHdOPo, EhoLJF);
            if (PHdOPo[0] > 7 || PHdOPo[0] < 0) {
                break;
            };
            if (PHdOPo[1] > 7 || PHdOPo[1] < 0) {
                break;
            };
            lGjFpn = Math.round(PHdOPo[0] + (PHdOPo[1] * 8));
            dgLdGd = '_' + lGjFpn;
            if (cfiLMN.hasOwnProperty(dgLdGd)) {
                if (aFmigA <= 0) {
                    aFmigA = cfiLMN[dgLdGd];
                    if (lfhCNa) {
                        if (aFmigA < 21) {
                            break;
                        }
                    } else {
                        if (aFmigA > 20) {
                            break;
                        }
                    };
                } else {
                    break;
                }
            } else {
                if (aFmigA > 0) {
                    khkhcP.fpMgcJ = true;
                };
                lcmkjE[dgLdGd] = aFmigA;
                CPagiO.push(lGjFpn);
            }
        };
        if (!NPicpE) {
            if (khkhcP.fpMgcJ) {
                var hkpnAN = null;
                CPagiO = [];
                mJeAlE = Object.keys(lcmkjE);
                bmfhpd = mJeAlE.length;
                for (fOGnCG = 0; fOGnCG < bmfhpd; fOGnCG++) {
                    kdbnIl = mJeAlE[fOGnCG];
                    if (lcmkjE[kdbnIl] > 0) {
                        lGjFpn = NmbiKM(kdbnIl.substring(1));
                        var llIIgc = this.bNNnfJ(lGjFpn);
                        var dJMcDC = {
                            AFmnNn: [],
                            fpMgcJ: false
                        };
                        if (EhoLJF[0] != 1 || EhoLJF[1] != 1) {
                            this.PjeOla([-1, -1], lfhCNa, llIIgc, dJMcDC, cfiLMN, true);
                        };
                        if (EhoLJF[0] != 1 || EhoLJF[1] != -1) {
                            this.PjeOla([-1, 1], lfhCNa, llIIgc, dJMcDC, cfiLMN, true);
                        };
                        if (EhoLJF[0] != -1 || EhoLJF[1] != 1) {
                            this.PjeOla([1, -1], lfhCNa, llIIgc, dJMcDC, cfiLMN, true);
                        };
                        if (EhoLJF[0] != -1 || EhoLJF[1] != -1) {
                            this.PjeOla([1, 1], lfhCNa, llIIgc, dJMcDC, cfiLMN, true);
                        };
                        if (dJMcDC.fpMgcJ) {
                            if (!hkpnAN) {
                                hkpnAN = {};
                            };
                            hkpnAN[kdbnIl] = true;
                        };
                        CPagiO.push(lGjFpn);
                    } else {
                        delete lcmkjE[kdbnIl];
                    }
                };
                if (hkpnAN) {
                    CPagiO = [];
                    mJeAlE = Object.keys(lcmkjE);
                    bmfhpd = mJeAlE.length;
                    for (fOGnCG = 0; fOGnCG < bmfhpd; fOGnCG++) {
                        kdbnIl = mJeAlE[fOGnCG];
                        if (hkpnAN.hasOwnProperty(kdbnIl)) {
                            CPagiO.push(NmbiKM(kdbnIl.substring(1)));
                        } else {
                            delete lcmkjE[kdbnIl];
                        }
                    };
                }
            };
        };
        for (kdbnIl in lcmkjE) {
            khkhcP[kdbnIl] = lcmkjE[kdbnIl];
        };
        bmfhpd = CPagiO.length;
        for (fOGnCG = 0; fOGnCG < bmfhpd; fOGnCG++) {
            khkhcP.AFmnNn.push(CPagiO[fOGnCG]);
        }
    };
    return function () {
        return new eAeFAO(new JpMdFf(arguments))
    };
})();
BLAZE.GoaAhe = GoaAhe;
var NmiACa = (function () {
    var PMFAbI = BLAZE.GetENV('PROJECT_CONTENT_URL');
    var dDFAkd = 10000;
    var CGMpPj = Math.round(dDFAkd * 0.1);
    var ljLfNo = 1 / dDFAkd;
    var ibgFKk = 1.3;
    var FEgCOl = 2.7;
    var cgCLNA = 0.7;
    var CiPeLK = [12, 10];
    var IOKBHp = CiPeLK[0] * CiPeLK[1];
    var abMndG = HAELdp.BObpdE(1.5 * dDFAkd);
    var FknbkJ = 0.7;
    var DgiCNk = 6;
    var eLiahC = (1 - FknbkJ) / DgiCNk;
    var iMgPoP = 1 / DgiCNk;
    var nHpnEC = 10;
    var JMeCBB = 160;
    var NHocha = 20;
    var JEpkfL = 1 * dDFAkd;
    var ogNmao = 100;
    var JfOHAI = 0.5;
    var JfnKmi = 1.2;
    var EhBAol = [160, 1140];
    var hhGIpP = 26;
    var EiDDdo = 220;
    var afLliH = 1.7;
    var IDGMhC = 0.004;
    var ooFOBc = 0.1;
    var HOKnla = 200;
    var oppODF = 1.2;
    var HFOgdh = 2;
    var CHfidh = 5;
    var AdnedG = {
        NEeGOB: ['pocket_1', 'pocket_2', 'pocket_3', 'pocket_4'],
        dchiKB: ['cue'],
        EPAaHk: ['table_border'],
        jFdnFM: ['ball_s1', 'ball_s2', 'ball_s3', 'ball_s4'],
        BkOeel: ['ball_m1', 'ball_m2', 'ball_m3', 'ball_m4', 'ball_m5'],
        ndNifi: ['ball_f1', 'ball_f2', 'ball_f3', 'ball_f4', 'ball_f5']
    };
    var EhGpIf = [['10% 100%'], ['10% 0%'], ['20% 100%'], ['20% 0%'], ['30% 100%'], ['30% 0%'], ['40% 100%'], ['40% 0%'], ['50% 100%'], ['50% 0%'], ['60% 100%'], ['60% 0%'], ['70% 100%'], ['70% 0%'], ['80% 100%'], ['80% 0%'], ['90% 100%'], ['90% 0%'], ['100% 100%'], ['100% 0%']];
    var BjmnkM = [];
    BjmnkM[1] = [60.9, 0.032, true, EhGpIf];
    BjmnkM[2] = [49.4, 0.04, true, EhGpIf];
    BjmnkM[3] = [41.54, 0.048, true, EhGpIf];
    BjmnkM[4] = [37.6, 0.04, true, EhGpIf];
    BjmnkM[5] = [34.1, 0.035, true, EhGpIf];
    BjmnkM[6] = [13.25, 0.04, true, EhGpIf];
    BjmnkM[7] = [23.38, 0.03, true, EhGpIf];
    var mKEgAF = [1800, 1000];
    var EeJJiE = [7, 4];
    var GdeJPB = [mKEgAF[0] * dDFAkd, mKEgAF[1] * dDFAkd];
    var nFhIkg = [Math.round(GdeJPB[0] / EeJJiE[0]), Math.round(GdeJPB[1] / EeJJiE[1])];
    var oHHiBg = 'billiards_ballset';
    var FiKoam = [5, 3];
    var dagePF = [];
    dagePF[0] = {
        hJAPBi: 25,
        pPGclC: [[1, 0], [2, 1], [3, 2], [4, 3], [5, 4], [6, 5], [7, 6], [8, 7], [9, 8], [1, 9], [1, 10], [1, 11], [1, 12], [1, 13], [1, 14], [1, 15]]
    };
    dagePF[1] = {
        hJAPBi: 25,
        pPGclC: [[1, 0], [2, 1], [3, 2], [4, 3], [5, 4], [6, 5], [7, 6], [8, 7], [9, 8], [1, 9], [1, 10], [1, 11], [1, 12], [1, 13], [1, 14], [1, 15]]
    };
    dagePF[2] = {
        hJAPBi: 27,
        pPGclC: [[14, 0], [1, 1], [1, 2], [1, 3], [1, 4], [1, 5], [1, 6], [1, 7], [1, 8], [1, 16], [1, 17], [1, 18], [1, 19], [1, 20], [1, 21], [1, 22]]
    };
    dagePF[3] = {
        hJAPBi: 26,
        pPGclC: [[1, 0], [14, -1], [10, -1]]
    };
    dagePF[4] = {
        hJAPBi: 25,
        pPGclC: [[1, 0], [2, 1], [3, 2], [4, 3], [5, 4], [6, 5], [7, 6], [8, 7], [9, 8], [1, 9]]
    };
    dagePF[5] = {
        hJAPBi: 22,
        pPGclC: [[1, 0], [2, -1], [7, -1], [6, -1], [3, -1], [13, -1], [9, -1], [12, -1], [11, -1], [10, -1]]
    };
    dagePF[6] = {
        hJAPBi: 25,
        pPGclC: [[1, 0], [10, -1], [10, -1], [10, -1], [10, -1], [10, -1], [9, -1], [9, -1], [9, -1], [9, -1], [9, -1], [14, -1], [14, -1], [14, -1], [14, -1], [14, -1]]
    };
    var apKgiH = [];
    apKgiH[0] = {
        eaGHGh: 0,
        gelDml: 0,
        opIBcp: 45,
        NFpaah: 1.2,
        fMHNgD: 0.13,
        kHEMgD: 2.0,
        AgkCiF: [[13477000, 4990000], [5670000, 5000000], [5210000, 4730000], [5210000, 5270000], [4740000, 4460000], [4760000, 5000000], [4740000, 5530000], [4280000, 4200000], [4300000, 4730000], [4300000, 5270000], [4280000, 5800000], [3820000, 3940000], [3830000, 4470000], [3840000, 5000000], [3830000, 5530000], [3820000, 6060000]],
        pPGclC: [[0, 0, 0], [1, 1, -1], [2, 2, -1], [3, 3, -1], [4, 4, -1], [5, 5, -1], [6, 6, -1], [7, 7, -1], [8, 8, 5], [9, 9, -1], [10, 10, -1], [11, 11, -1], [12, 12, -1], [13, 13, -1], [14, 14, -1], [15, 15, -1]]
    };
    apKgiH[1] = {
        eaGHGh: 1,
        gelDml: 1,
        opIBcp: 45,
        NFpaah: 1.2,
        fMHNgD: 0.13,
        kHEMgD: 2.0,
        AgkCiF: [[13477000, 4990000], [5670000, 5000000], [5210000, 4730000], [5210000, 5270000], [4740000, 4460000], [4760000, 5000000], [4740000, 5530000], [4280000, 4200000], [4300000, 4730000], [4300000, 5270000], [4280000, 5800000], [3820000, 3940000], [3830000, 4470000], [3840000, 5000000], [3830000, 5530000], [3820000, 6060000]],
        pPGclC: [[0, 0, 0], [1, 1, -1], [2, 2, -1], [3, 3, -1], [4, 4, -1], [5, 5, -1], [6, 6, -1], [7, 7, -1], [8, 8, -1], [9, 9, -1], [10, 10, -1], [11, 11, -1], [12, 12, -1], [13, 13, -1], [14, 14, -1], [15, 15, -1]]
    };
    apKgiH[2] = {
        eaGHGh: 2,
        gelDml: 2,
        opIBcp: 45,
        NFpaah: 1.2,
        fMHNgD: 0.13,
        kHEMgD: 2.0,
        AgkCiF: [[13477000, 4990000], [5790000, 5000000], [5300000, 4710000], [5300000, 5290000], [4800000, 4420000], [4820000, 5000000], [4800000, 5570000], [4310000, 4140000], [4330000, 4710000], [4330000, 5290000], [4310000, 5860000], [3820000, 3860000], [3830000, 4430000], [3840000, 5000000], [3830000, 5570000], [3820000, 6140000]],
        pPGclC: [[0, 0, 0], [1, 1, -1], [2, 2, -1], [3, 3, -1], [4, 4, -1], [5, 5, -1], [6, 6, -1], [7, 7, -1], [8, 8, -1], [9, 9, -1], [10, 10, -1], [11, 11, -1], [12, 12, -1], [13, 13, -1], [14, 14, -1], [15, 15, -1]]
    };
    apKgiH[3] = {
        eaGHGh: 3,
        gelDml: 3,
        opIBcp: 45,
        NFpaah: 1.2,
        fMHNgD: 0.13,
        kHEMgD: 2.0,
        AgkCiF: [[13125000, 5000000], [4850000, 5000000], [4850000, 3720000]],
        pPGclC: [[0, 0, 0], [1, 1, 1], [2, 2, 2]]
    };
    apKgiH[4] = {
        eaGHGh: 4,
        gelDml: 0,
        opIBcp: 45,
        NFpaah: 1.2,
        fMHNgD: 0.13,
        kHEMgD: 2.0,
        AgkCiF: [[9000000, 6460000], [9000000, 4850000], [9270000, 4400000], [8730000, 4400000], [9530000, 3940000], [9000000, 3950000], [8470000, 3940000], [9780000, 3470000], [9260000, 3490000], [8740000, 3490000], [8220000, 3470000], [10040000, 3010000], [9520000, 3020000], [9000000, 3010000], [8480000, 3020000], [7960000, 3010000]],
        pPGclC: [[0, 0, 0], [1, 1, -1], [2, 2, -1], [3, 3, -1], [4, 4, -1], [5, 5, -1], [6, 6, -1], [7, 7, -1], [8, 8, -1], [9, 9, -1], [10, 10, -1], [11, 11, -1], [12, 12, -1], [13, 13, -1], [14, 14, -1], [15, 15, -1]]
    };
    apKgiH[5] = {
        eaGHGh: 5,
        gelDml: 5,
        opIBcp: 45,
        NFpaah: 1.2,
        fMHNgD: 0.13,
        kHEMgD: 1.4,
        AgkCiF: [[14700000, 5000000], [13150000, 3420000], [13150000, 6580000], [13150000, 5000000], [9000000, 5000000], [5870000, 5000000], [2220000, 5000000], [5390000, 5000000], [4980000, 4760000], [4980000, 5240000], [4570000, 4530000], [4580000, 5000000], [4570000, 5470000], [4160000, 4280000], [4170000, 4760000], [4170000, 5240000], [4160000, 5720000], [3750000, 4060000], [3760000, 4530000], [3750000, 5000000], [3760000, 5470000], [3750000, 5940000]],
        pPGclC: [[0, 0, 0], [1, 1, 1], [2, 2, 2], [3, 3, 3], [4, 4, 4], [5, 5, 5], [6, 6, 6], [7, 9, -1], [8, 9, -1], [9, 9, -1], [10, 9, -1], [11, 9, -1], [12, 9, -1], [13, 9, -1], [14, 9, -1], [15, 9, -1], [16, 9, -1], [17, 9, -1], [18, 9, -1], [19, 9, -1], [20, 9, -1], [21, 9, -1]]
    };
    apKgiH[6] = {
        eaGHGh: 5,
        gelDml: 5,
        opIBcp: 45,
        NFpaah: 1.2,
        fMHNgD: 0.13,
        kHEMgD: 1.4,
        AgkCiF: [[14700000, 5000000], [13150000, 3420000], [13150000, 6580000], [13150000, 5000000], [9000000, 5000000], [5870000, 5000000], [2220000, 5000000], [7430000, 5000000], [10570000, 5000000], [5390000, 5000000], [4980000, 4760000], [4980000, 5240000], [4570000, 4530000], [4580000, 5000000], [4570000, 5470000], [4160000, 4280000], [4170000, 4760000], [4170000, 5240000], [4160000, 5720000], [3750000, 4060000], [3760000, 4530000], [3750000, 5000000], [3760000, 5470000], [3750000, 5940000]],
        pPGclC: [[0, 0, 0], [1, 1, 1], [2, 2, 2], [3, 3, 3], [4, 4, 4], [5, 5, 5], [6, 6, 6], [7, 7, 7], [8, 8, 8], [9, 9, -1], [10, 9, -1], [11, 9, -1], [12, 9, -1], [13, 9, -1], [14, 9, -1], [15, 9, -1], [16, 9, -1], [17, 9, -1], [18, 9, -1], [19, 9, -1], [20, 9, -1], [21, 9, -1], [22, 9, -1], [23, 9, -1]]
    };
    apKgiH[7] = {
        eaGHGh: 0,
        gelDml: 4,
        opIBcp: 45,
        NFpaah: 1.2,
        fMHNgD: 0.13,
        kHEMgD: 2.0,
        AgkCiF: [[13477000, 5000000], [5670000, 5000000], [4300000, 5260000], [4750000, 4470000], [3840000, 5000000], [5210000, 5260000], [4300000, 4740000], [5210000, 4740000], [4750000, 5530000], [4760000, 5000000]],
        pPGclC: [[0, 0, 0], [1, 1, 1], [2, 2, 2], [3, 3, 3], [4, 4, 4], [5, 5, 5], [6, 6, 6], [7, 7, 7], [8, 8, 8], [9, 9, 9]]
    };
    apKgiH[8] = {
        eaGHGh: 0,
        gelDml: 6,
        opIBcp: 45,
        NFpaah: 1.2,
        fMHNgD: 0.13,
        kHEMgD: 2.0,
        AgkCiF: [[13477000, 4990000], [5670000, 5000000], [5210000, 4730000], [5210000, 5270000], [4740000, 4460000], [4760000, 5000000], [4740000, 5530000], [4280000, 4200000], [4300000, 4730000], [4300000, 5270000], [4280000, 5800000], [3820000, 3940000], [3830000, 4470000], [3840000, 5000000], [3830000, 5530000], [3820000, 6060000]],
        pPGclC: [[0, 0, 0], [1, 1, -1], [2, 2, -1], [3, 3, -1], [4, 4, -1], [5, 5, -1], [6, 6, -1], [7, 7, -1], [8, 8, 5], [9, 9, -1], [10, 10, -1], [11, 11, -1], [12, 12, -1], [13, 13, -1], [14, 14, -1], [15, 15, -1]]
    };
    apKgiH[9] = {
        eaGHGh: 0,
        gelDml: 4,
        opIBcp: 45,
        NFpaah: 1.2,
        fMHNgD: 0.13,
        kHEMgD: 2.0,
        AgkCiF: [[13477000, 5000000], [5670000, 5000000], [4300000, 5260000], [4750000, 4470000], [3840000, 5000000], [5210000, 5260000], [4300000, 4740000], [5210000, 4740000], [4750000, 5530000], [4760000, 5000000]],
        pPGclC: [[0, 0, 0], [1, 1, -1], [2, 2, -1], [3, 3, -1], [4, 4, -1], [5, 5, -1], [6, 6, -1], [7, 7, -1], [8, 8, -1], [9, 9, -1]]
    };
    var MnNneL = [];
    MnNneL[0] = {
        jAnOai: 45,
        BNECAi: [[1030000, 1030000], [16970000, 8970000]],
        FgAmGe: [[13130000, 1030000], [16970000, 8970000]],
        kEKLHa: [[13120000, 5000000], [13120000, 3420000]],
        IimcEf: {
            _1: [980000, 980000],
            _2: [980000, 9020000],
            _3: [9000000, 750000],
            _4: [9000000, 9250000],
            _5: [17020000, 980000],
            _6: [17020000, 9020000]
        },
        ekbEHn: {
            _1: [635000, 635000],
            _3: [9000000, 390000],
            _5: [17365000, 635000],
            _6: [17365000, 9365000],
            _4: [9000000, 9610000],
            _2: [635000, 9365000]
        },
        Imlbnm: [[1000000, 1280000, 0, -70000, 20000, 44400000000, 72801.09889280518], [980000, 1210000, 0, -270000, 270000, -62100000000, 381837.66184073564], [710000, 940000, 1, -230000, -230000, 379500000000, 325269.11934581184], [940000, 710000, 0, 270000, -270000, -62100000000, 381837.66184073564], [1210000, 980000, 0, 20000, -70000, 44400000000, 72801.09889280518], [1280000, 1000000, 0, 0, -7320000, 7320000000000, 7320000], [8600000, 1000000, 0, -80000, -110000, 798000000000, 136014.70508735444], [8710000, 920000, 0, -330000, -70000, 2938700000000, 337342.55586866], [8780000, 590000, 3, 0, -440000, 259600000000, 440000], [9220000, 590000, 0, 330000, -70000, -3001300000000, 337342.55586866], [9290000, 920000, 0, 80000, -110000, -642000000000, 136014.70508735444], [9400000, 1000000, 0, 0, -7320000, 7320000000000, 7320000], [16720000, 1000000, 0, -20000, -70000, 404400000000, 72801.09889280518], [16790000, 980000, 0, -270000, -270000, 4797900000000, 381837.66184073564], [17060000, 710000, 5, 230000, -230000, -3760500000000, 325269.11934581184], [17290000, 940000, 0, 270000, 270000, -4922100000000, 381837.66184073564], [17020000, 1210000, 0, 70000, 20000, -1215600000000, 72801.09889280518], [17000000, 1280000, 0, 7440000, 0, -126480000000000, 7440000], [17000000, 8720000, 0, 70000, -20000, -1015600000000, 72801.09889280518], [17020000, 8790000, 0, 270000, -270000, -2222100000000, 381837.66184073564], [17290000, 9060000, 6, 230000, 230000, -6060500000000, 325269.11934581184], [17060000, 9290000, 0, -270000, 270000, 2097900000000, 381837.66184073564], [16790000, 9020000, 0, -20000, 70000, -295600000000, 72801.09889280518], [16720000, 9000000, 0, 0, 7320000, -65880000000000, 7320000], [9400000, 9000000, 0, 80000, 110000, -1742000000000, 136014.70508735444], [9290000, 9080000, 0, 330000, 70000, -3701300000000, 337342.55586866], [9220000, 9410000, 4, 0, 440000, -4140400000000, 440000], [8780000, 9410000, 0, -330000, 70000, 2238700000000, 337342.55586866], [8710000, 9080000, 0, -80000, 110000, -302000000000, 136014.70508735444], [8600000, 9000000, 0, 0, 7320000, -65880000000000, 7320000], [1280000, 9000000, 0, 20000, 70000, -655600000000, 72801.09889280518], [1210000, 9020000, 0, 270000, 270000, -2762100000000, 381837.66184073564], [940000, 9290000, 2, -230000, 230000, -1920500000000, 325269.11934581184], [710000, 9060000, 0, -270000, -270000, 2637900000000, 381837.66184073564], [980000, 8790000, 0, -70000, -20000, 244400000000, 72801.09889280518], [1000000, 8720000, 0, -7440000, 0, 7440000000000, 7440000], [1000000, 1280000, 0]],
        JHiMkK: [[[0, 1, 2, 3, 4, 5, 35], [0, 1, 2, 3, 4, 5, 35], null, null, null, null, null, [0, 1, 2, 3, 4, 5, 35], [0, 1, 2, 3, 4, 5, 35], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null], [[5, 0, 1, 2, 3, 4, 35], [5], [5], null, null, null, null, [5, 35], [5], [5], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null], [null, [5], [5], [5, 6, 7, 8, 9, 10, 11], null, null, null, null, [5], [5], [5], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null], [null, null, [5, 6, 7, 8, 9, 10, 11], [5, 6, 7, 8, 9, 10, 11], [5, 6, 7, 8, 9, 10, 11], null, null, null, null, [5, 6, 7, 8, 9, 10, 11], [5, 6, 7, 8, 9, 10, 11], [5, 6, 7, 8, 9, 10, 11], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null], [null, null, null, [11, 5, 6, 7, 8, 9, 10], [11], [11], null, null, null, null, [11], [11], [11], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null], [null, null, null, null, [11], [11], [11, 12, 13, 14, 15, 16, 17], null, null, null, null, [11], [11], [11, 17], null, null, null, null, null, null, null, null, null, null, null, null, null, null], [null, null, null, null, null, [11, 12, 13, 14, 15, 16, 17], [11, 12, 13, 14, 15, 16, 17], null, null, null, null, null, [11, 12, 13, 14, 15, 16, 17], [11, 12, 13, 14, 15, 16, 17], null, null, null, null, null, null, null, null, null, null, null, null, null, null], [[35, 0, 1, 2, 3, 4, 5], [35, 5], null, null, null, null, null, [35], [35], null, null, null, null, null, [35], [35], null, null, null, null, null, null, null, null, null, null, null, null], [[0, 1, 2, 3, 4, 5, 35], [5], [5], null, null, null, null, [35], null, null, null, null, null, null, [35], null, null, null, null, null, null, null, null, null, null, null, null, null], [null, [5], [5], [5, 6, 7, 8, 9, 10, 11], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null], [null, null, [5], [5, 6, 7, 8, 9, 10, 11], [11], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null], [null, null, null, [5, 6, 7, 8, 9, 10, 11], [11], [11], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null], [null, null, null, null, [11], [11], [11, 12, 13, 14, 15, 16, 17], null, null, null, null, null, null, [17], null, null, null, null, null, null, [17], null, null, null, null, null, null, null], [null, null, null, null, null, [17, 11], [17, 11, 12, 13, 14, 15, 16], null, null, null, null, null, [17], [17], null, null, null, null, null, [17], [17], null, null, null, null, null, null, null], [null, null, null, null, null, null, null, [35], [35], null, null, null, null, null, [35], [35], null, null, null, null, null, [35, 29, 30, 31, 32, 33, 34], [35, 29], null, null, null, null, null], [null, null, null, null, null, null, null, [35], null, null, null, null, null, null, [35], null, null, null, null, null, null, [29, 30, 31, 32, 33, 34, 35], [29], [29], null, null, null, null], [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [29], [29], [23, 24, 25, 26, 27, 28, 29], null, null, null], [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [29], [23, 24, 25, 26, 27, 28, 29], [23], null, null], [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [23, 24, 25, 26, 27, 28, 29], [23], [23], null], [null, null, null, null, null, null, null, null, null, null, null, null, null, [17], null, null, null, null, null, null, [17], null, null, null, null, [23], [23], [17, 18, 19, 20, 21, 22, 23]], [null, null, null, null, null, null, null, null, null, null, null, null, [17], [17], null, null, null, null, null, [17], [17], null, null, null, null, null, [17, 23], [17, 18, 19, 20, 21, 22, 23]], [null, null, null, null, null, null, null, null, null, null, null, null, null, null, [29, 30, 31, 32, 33, 34, 35], [29, 30, 31, 32, 33, 34, 35], null, null, null, null, null, [29, 30, 31, 32, 33, 34, 35], [29, 30, 31, 32, 33, 34, 35], null, null, null, null, null], [null, null, null, null, null, null, null, null, null, null, null, null, null, null, [29, 35], [29], [29], null, null, null, null, [29, 30, 31, 32, 33, 34, 35], [29], [29], null, null, null, null], [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [29], [29], [29], null, null, null, null, [29], [29], [29, 23, 24, 25, 26, 27, 28], null, null, null], [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [23, 24, 25, 26, 27, 28, 29], [23, 24, 25, 26, 27, 28, 29], [23, 24, 25, 26, 27, 28, 29], null, null, null, null, [23, 24, 25, 26, 27, 28, 29], [23, 24, 25, 26, 27, 28, 29], [23, 24, 25, 26, 27, 28, 29], null, null], [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [23], [23], [23], null, null, null, null, [23, 24, 25, 26, 27, 28, 29], [23], [23], null], [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [23], [23], [23, 17], null, null, null, null, [23], [23], [23, 17, 18, 19, 20, 21, 22]], [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [17, 18, 19, 20, 21, 22, 23], [17, 18, 19, 20, 21, 22, 23], null, null, null, null, null, [17, 18, 19, 20, 21, 22, 23], [17, 18, 19, 20, 21, 22, 23]]]
    };
    MnNneL[1] = {
        jAnOai: 55,
        BNECAi: [[1160000, 1160000], [16840000, 8840000]],
        FgAmGe: [[13060000, 1160000], [16840000, 8840000]],
        kEKLHa: [[13050000, 5000000], [13050000, 3150000]],
        IimcEf: {
            _1: [1150000, 1150000],
            _2: [1150000, 8850000],
            _3: [9000000, 900000],
            _4: [9000000, 9100000],
            _5: [16850000, 1150000],
            _6: [16850000, 8850000]
        },
        ekbEHn: {
            _1: [750000, 750000],
            _3: [9000000, 460000],
            _5: [17250000, 750000],
            _6: [17250000, 9250000],
            _4: [9000000, 9540000],
            _2: [750000, 9250000]
        },
        Imlbnm: [[1150000, 1420000, 0, -60000, 30000, 26400000000, 67082.03932499369], [1120000, 1360000, 0, -320000, 320000, -76800000000, 452548.3399593904], [800000, 1040000, 1, -240000, -240000, 441600000000, 339411.2549695428], [1040000, 800000, 0, 320000, -320000, -76800000000, 452548.3399593904], [1360000, 1120000, 0, 30000, -60000, 26400000000, 67082.03932499369], [1420000, 1150000, 0, 0, -7150000, 8222500000000, 7150000], [8570000, 1150000, 0, -90000, -110000, 897800000000, 142126.70403551895], [8680000, 1060000, 0, -410000, -100000, 3664800000000, 422018.95692018385], [8780000, 650000, 3, 0, -440000, 286000000000, 440000], [9220000, 650000, 0, 410000, -100000, -3715200000000, 422018.95692018385], [9320000, 1060000, 0, 90000, -110000, -722200000000, 142126.70403551895], [9430000, 1150000, 0, 0, -7150000, 8222500000000, 7150000], [16580000, 1150000, 0, -30000, -60000, 566400000000, 67082.03932499369], [16640000, 1120000, 0, -320000, -320000, 5683200000000, 452548.3399593904], [16960000, 800000, 5, 240000, -240000, -3878400000000, 339411.2549695428], [17200000, 1040000, 0, 320000, 320000, -5836800000000, 452548.3399593904], [16880000, 1360000, 0, 60000, 30000, -1053600000000, 67082.03932499369], [16850000, 1420000, 0, 7160000, 0, -120646000000000, 7160000], [16850000, 8580000, 0, 60000, -30000, -753600000000, 67082.03932499369], [16880000, 8640000, 0, 320000, -320000, -2636800000000, 452548.3399593904], [17200000, 8960000, 6, 240000, 240000, -6278400000000, 339411.2549695428], [16960000, 9200000, 0, -320000, 320000, 2483200000000, 452548.3399593904], [16640000, 8880000, 0, -30000, 60000, -33600000000, 67082.03932499369], [16580000, 8850000, 0, 0, 7150000, -63277500000000, 7150000], [9430000, 8850000, 0, 90000, 110000, -1822200000000, 142126.70403551895], [9320000, 8940000, 0, 410000, 100000, -4715200000000, 422018.95692018385], [9220000, 9350000, 4, 0, 440000, -4114000000000, 440000], [8780000, 9350000, 0, -410000, 100000, 2664800000000, 422018.95692018385], [8680000, 8940000, 0, -90000, 110000, -202200000000, 142126.70403551895], [8570000, 8850000, 0, 0, 7150000, -63277500000000, 7150000], [1420000, 8850000, 0, 30000, 60000, -573600000000, 67082.03932499369], [1360000, 8880000, 0, 320000, 320000, -3276800000000, 452548.3399593904], [1040000, 9200000, 2, -240000, 240000, -1958400000000, 339411.2549695428], [800000, 8960000, 0, -320000, -320000, 3123200000000, 452548.3399593904], [1120000, 8640000, 0, -60000, -30000, 326400000000, 67082.03932499369], [1150000, 8580000, 0, -7160000, 0, 8234000000000, 7160000], [1150000, 1420000, 0]],
        JHiMkK: [[[0, 1, 2, 3, 4, 5, 35], [0, 1, 2, 3, 4, 5, 35], null, null, null, null, null, [0, 1, 2, 3, 4, 5, 35], [0, 1, 2, 3, 4, 5, 35], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null], [[5, 0, 1, 2, 3, 4, 35], [5], [5], null, null, null, null, [5, 35], [5], [5], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null], [null, [5], [5], [5, 6, 7, 8, 9, 10, 11], null, null, null, null, [5], [5], [5], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null], [null, null, [5, 6, 7, 8, 9, 10, 11], [5, 6, 7, 8, 9, 10, 11], [5, 6, 7, 8, 9, 10, 11], null, null, null, null, [5, 6, 7, 8, 9, 10, 11], [5, 6, 7, 8, 9, 10, 11], [5, 6, 7, 8, 9, 10, 11], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null], [null, null, null, [11, 5, 6, 7, 8, 9, 10], [11], [11], null, null, null, null, [11], [11], [11], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null], [null, null, null, null, [11], [11], [11, 12, 13, 14, 15, 16, 17], null, null, null, null, [11], [11], [11, 17], null, null, null, null, null, null, null, null, null, null, null, null, null, null], [null, null, null, null, null, [11, 12, 13, 14, 15, 16, 17], [11, 12, 13, 14, 15, 16, 17], null, null, null, null, null, [11, 12, 13, 14, 15, 16, 17], [11, 12, 13, 14, 15, 16, 17], null, null, null, null, null, null, null, null, null, null, null, null, null, null], [[35, 0, 1, 2, 3, 4, 5], [35, 5], null, null, null, null, null, [35], [35], null, null, null, null, null, [35], [35], null, null, null, null, null, null, null, null, null, null, null, null], [[0, 1, 2, 3, 4, 5, 35], [5], [5], null, null, null, null, [35], null, null, null, null, null, null, [35], null, null, null, null, null, null, null, null, null, null, null, null, null], [null, [5], [5], [5, 6, 7, 8, 9, 10, 11], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null], [null, null, [5], [5, 6, 7, 8, 9, 10, 11], [11], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null], [null, null, null, [5, 6, 7, 8, 9, 10, 11], [11], [11], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null], [null, null, null, null, [11], [11], [11, 12, 13, 14, 15, 16, 17], null, null, null, null, null, null, [17], null, null, null, null, null, null, [17], null, null, null, null, null, null, null], [null, null, null, null, null, [17, 11], [17, 11, 12, 13, 14, 15, 16], null, null, null, null, null, [17], [17], null, null, null, null, null, [17], [17], null, null, null, null, null, null, null], [null, null, null, null, null, null, null, [35], [35], null, null, null, null, null, [35], [35], null, null, null, null, null, [35, 29, 30, 31, 32, 33, 34], [35, 29], null, null, null, null, null], [null, null, null, null, null, null, null, [35], null, null, null, null, null, null, [35], null, null, null, null, null, null, [29, 30, 31, 32, 33, 34, 35], [29], [29], null, null, null, null], [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [29], [29], [23, 24, 25, 26, 27, 28, 29], null, null, null], [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [29], [23, 24, 25, 26, 27, 28, 29], [23], null, null], [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [23, 24, 25, 26, 27, 28, 29], [23], [23], null], [null, null, null, null, null, null, null, null, null, null, null, null, null, [17], null, null, null, null, null, null, [17], null, null, null, null, [23], [23], [17, 18, 19, 20, 21, 22, 23]], [null, null, null, null, null, null, null, null, null, null, null, null, [17], [17], null, null, null, null, null, [17], [17], null, null, null, null, null, [17, 23], [17, 18, 19, 20, 21, 22, 23]], [null, null, null, null, null, null, null, null, null, null, null, null, null, null, [29, 30, 31, 32, 33, 34, 35], [29, 30, 31, 32, 33, 34, 35], null, null, null, null, null, [29, 30, 31, 32, 33, 34, 35], [29, 30, 31, 32, 33, 34, 35], null, null, null, null, null], [null, null, null, null, null, null, null, null, null, null, null, null, null, null, [29, 35], [29], [29], null, null, null, null, [29, 30, 31, 32, 33, 34, 35], [29], [29], null, null, null, null], [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [29], [29], [29], null, null, null, null, [29], [29], [29, 23, 24, 25, 26, 27, 28], null, null, null], [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [23, 24, 25, 26, 27, 28, 29], [23, 24, 25, 26, 27, 28, 29], [23, 24, 25, 26, 27, 28, 29], null, null, null, null, [23, 24, 25, 26, 27, 28, 29], [23, 24, 25, 26, 27, 28, 29], [23, 24, 25, 26, 27, 28, 29], null, null], [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [23], [23], [23], null, null, null, null, [23, 24, 25, 26, 27, 28, 29], [23], [23], null], [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [23], [23], [23, 17], null, null, null, null, [23], [23], [23, 17, 18, 19, 20, 21, 22]], [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [17, 18, 19, 20, 21, 22, 23], [17, 18, 19, 20, 21, 22, 23], null, null, null, null, null, [17, 18, 19, 20, 21, 22, 23], [17, 18, 19, 20, 21, 22, 23]]]
    };
    MnNneL[2] = {
        jAnOai: 45,
        BNECAi: [[1050000, 1050000], [16950000, 8950000]],
        FgAmGe: [[13130000, 1050000], [16950000, 8950000]],
        kEKLHa: [[13120000, 5000000], [13120000, 3420000]],
        IimcEf: {
            _1: [1000000, 1000000],
            _2: [1000000, 9000000],
            _3: [9000000, 750000],
            _4: [9000000, 9250000],
            _5: [17000000, 1000000],
            _6: [17000000, 9000000]
        },
        ekbEHn: {
            _1: [635000, 635000],
            _3: [9000000, 390000],
            _5: [17365000, 635000],
            _6: [17365000, 9365000],
            _4: [9000000, 9610000],
            _2: [635000, 9365000]
        },
        Imlbnm: [[1020000, 1230000, 0, -80000, 30000, 44700000000, 85440.03745317532], [990000, 1150000, 0, -280000, 280000, -44800000000, 395979.7974644666], [710000, 870000, 1, -160000, -160000, 252800000000, 226274.1699796952], [870000, 710000, 0, 280000, -280000, -44800000000, 395979.7974644666], [1150000, 990000, 0, 30000, -80000, 44700000000, 85440.03745317532], [1230000, 1020000, 0, 0, -7390000, 7537800000000, 7390000], [8620000, 1020000, 0, -120000, -140000, 1177200000000, 184390.88914585774], [8760000, 900000, 0, -320000, -60000, 2857200000000, 325576.4119219941], [8820000, 580000, 3, 0, -360000, 208800000000, 360000], [9180000, 580000, 0, 320000, -60000, -2902800000000, 325576.4119219941], [9240000, 900000, 0, 120000, -140000, -982800000000, 184390.88914585774], [9380000, 1020000, 0, 0, -7390000, 7537800000000, 7390000], [16770000, 1020000, 0, -30000, -80000, 584700000000, 85440.03745317532], [16850000, 990000, 0, -280000, -280000, 4995200000000, 395979.7974644666], [17130000, 710000, 5, 160000, -160000, -2627200000000, 226274.1699796952], [17290000, 870000, 0, 280000, 280000, -5084800000000, 395979.7974644666], [17010000, 1150000, 0, 80000, 30000, -1395300000000, 85440.03745317532], [16980000, 1230000, 0, 7540000, 0, -128029200000000, 7540000], [16980000, 8770000, 0, 80000, -30000, -1095300000000, 85440.03745317532], [17010000, 8850000, 0, 280000, -280000, -2284800000000, 395979.7974644666], [17290000, 9130000, 6, 160000, 160000, -4227200000000, 226274.1699796952], [17130000, 9290000, 0, -280000, 280000, 2195200000000, 395979.7974644666], [16850000, 9010000, 0, -30000, 80000, -215300000000, 85440.03745317532], [16770000, 8980000, 0, 0, 7390000, -66362200000000, 7390000], [9380000, 8980000, 0, 120000, 140000, -2382800000000, 184390.88914585774], [9240000, 9100000, 0, 320000, 60000, -3502800000000, 325576.4119219941], [9180000, 9420000, 4, 0, 360000, -3391200000000, 360000], [8820000, 9420000, 0, -320000, 60000, 2257200000000, 325576.4119219941], [8760000, 9100000, 0, -120000, 140000, -222800000000, 184390.88914585774], [8620000, 8980000, 0, 0, 7390000, -66362200000000, 7390000], [1230000, 8980000, 0, 30000, 80000, -755300000000, 85440.03745317532], [1150000, 9010000, 0, 280000, 280000, -2844800000000, 395979.7974644666], [870000, 9290000, 2, -160000, 160000, -1347200000000, 226274.1699796952], [710000, 9130000, 0, -280000, -280000, 2755200000000, 395979.7974644666], [990000, 8850000, 0, -80000, -30000, 344700000000, 85440.03745317532], [1020000, 8770000, 0, -7540000, 0, 7690800000000, 7540000], [1020000, 1230000, 0]],
        JHiMkK: [[[0, 1, 2, 3, 4, 5, 35], [0, 1, 2, 3, 4, 5, 35], null, null, null, null, null, [0, 1, 2, 3, 4, 5, 35], [0, 1, 2, 3, 4, 5, 35], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null], [[5, 0, 1, 2, 3, 4, 35], [5], [5], null, null, null, null, [5, 35], [5], [5], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null], [null, [5], [5], [5, 6, 7, 8, 9, 10, 11], null, null, null, null, [5], [5], [5], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null], [null, null, [5, 6, 7, 8, 9, 10, 11], [5, 6, 7, 8, 9, 10, 11], [5, 6, 7, 8, 9, 10, 11], null, null, null, null, [5, 6, 7, 8, 9, 10, 11], [5, 6, 7, 8, 9, 10, 11], [5, 6, 7, 8, 9, 10, 11], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null], [null, null, null, [11, 5, 6, 7, 8, 9, 10], [11], [11], null, null, null, null, [11], [11], [11], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null], [null, null, null, null, [11], [11], [11, 12, 13, 14, 15, 16, 17], null, null, null, null, [11], [11], [11, 17], null, null, null, null, null, null, null, null, null, null, null, null, null, null], [null, null, null, null, null, [11, 12, 13, 14, 15, 16, 17], [11, 12, 13, 14, 15, 16, 17], null, null, null, null, null, [11, 12, 13, 14, 15, 16, 17], [11, 12, 13, 14, 15, 16, 17], null, null, null, null, null, null, null, null, null, null, null, null, null, null], [[35, 0, 1, 2, 3, 4, 5], [35, 5], null, null, null, null, null, [35], [35], null, null, null, null, null, [35], [35], null, null, null, null, null, null, null, null, null, null, null, null], [[0, 1, 2, 3, 4, 5, 35], [5], [5], null, null, null, null, [35], null, null, null, null, null, null, [35], null, null, null, null, null, null, null, null, null, null, null, null, null], [null, [5], [5], [5, 6, 7, 8, 9, 10, 11], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null], [null, null, [5], [5, 6, 7, 8, 9, 10, 11], [11], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null], [null, null, null, [5, 6, 7, 8, 9, 10, 11], [11], [11], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null], [null, null, null, null, [11], [11], [11, 12, 13, 14, 15, 16, 17], null, null, null, null, null, null, [17], null, null, null, null, null, null, [17], null, null, null, null, null, null, null], [null, null, null, null, null, [17, 11], [17, 11, 12, 13, 14, 15, 16], null, null, null, null, null, [17], [17], null, null, null, null, null, [17], [17], null, null, null, null, null, null, null], [null, null, null, null, null, null, null, [35], [35], null, null, null, null, null, [35], [35], null, null, null, null, null, [35, 29, 30, 31, 32, 33, 34], [35, 29], null, null, null, null, null], [null, null, null, null, null, null, null, [35], null, null, null, null, null, null, [35], null, null, null, null, null, null, [29, 30, 31, 32, 33, 34, 35], [29], [29], null, null, null, null], [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [29], [29], [23, 24, 25, 26, 27, 28, 29], null, null, null], [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [29], [23, 24, 25, 26, 27, 28, 29], [23], null, null], [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [23, 24, 25, 26, 27, 28, 29], [23], [23], null], [null, null, null, null, null, null, null, null, null, null, null, null, null, [17], null, null, null, null, null, null, [17], null, null, null, null, [23], [23], [17, 18, 19, 20, 21, 22, 23]], [null, null, null, null, null, null, null, null, null, null, null, null, [17], [17], null, null, null, null, null, [17], [17], null, null, null, null, null, [17, 23], [17, 18, 19, 20, 21, 22, 23]], [null, null, null, null, null, null, null, null, null, null, null, null, null, null, [29, 30, 31, 32, 33, 34, 35], [29, 30, 31, 32, 33, 34, 35], null, null, null, null, null, [29, 30, 31, 32, 33, 34, 35], [29, 30, 31, 32, 33, 34, 35], null, null, null, null, null], [null, null, null, null, null, null, null, null, null, null, null, null, null, null, [29, 35], [29], [29], null, null, null, null, [29, 30, 31, 32, 33, 34, 35], [29], [29], null, null, null, null], [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [29], [29], [29], null, null, null, null, [29], [29], [29, 23, 24, 25, 26, 27, 28], null, null, null], [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [23, 24, 25, 26, 27, 28, 29], [23, 24, 25, 26, 27, 28, 29], [23, 24, 25, 26, 27, 28, 29], null, null, null, null, [23, 24, 25, 26, 27, 28, 29], [23, 24, 25, 26, 27, 28, 29], [23, 24, 25, 26, 27, 28, 29], null, null], [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [23], [23], [23], null, null, null, null, [23, 24, 25, 26, 27, 28, 29], [23], [23], null], [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [23], [23], [23, 17], null, null, null, null, [23], [23], [23, 17, 18, 19, 20, 21, 22]], [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [17, 18, 19, 20, 21, 22, 23], [17, 18, 19, 20, 21, 22, 23], null, null, null, null, null, [17, 18, 19, 20, 21, 22, 23], [17, 18, 19, 20, 21, 22, 23]]]
    };
    MnNneL[3] = {
        jAnOai: 45,
        BNECAi: [[1020000, 1020000], [16980000, 8980000]],
        FgAmGe: [[13130000, 1020000], [16980000, 8980000]],
        kEKLHa: [[13120000, 5000000], [13120000, 3420000]],
        IimcEf: {},
        ekbEHn: {},
        Imlbnm: [[1010000, 1010000, null, 0, -15980000, 16139800000000, 15980000], [16990000, 1010000, null, 7980000, 0, -135580200000000, 7980000], [16990000, 8990000, null, 0, 15980000, -143660200000000, 15980000], [1010000, 8990000, null, -7980000, 0, 8059800000000, 7980000], [1010000, 1010000, null]],
        JHiMkK: [[[0, 3], [0, 3], null, null, null, null, null, [0, 3], [0, 3], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null], [[0, 3], [0], [0], null, null, null, null, [0, 3], [0], [0], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null], [null, [0], [0], [0], null, null, null, null, [0], [0], [0], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null], [null, null, [0], [0], [0], null, null, null, null, [0], [0], [0], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null], [null, null, null, [0], [0], [0], null, null, null, null, [0], [0], [0], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null], [null, null, null, null, [0], [0], [0, 1], null, null, null, null, [0], [0], [0, 1], null, null, null, null, null, null, null, null, null, null, null, null, null, null], [null, null, null, null, null, [0, 1], [0, 1], null, null, null, null, null, [0, 1], [0, 1], null, null, null, null, null, null, null, null, null, null, null, null, null, null], [[3, 0], [3, 0], null, null, null, null, null, [3], [3], null, null, null, null, null, [3], [3], null, null, null, null, null, null, null, null, null, null, null, null], [[0, 3], [0], [0], null, null, null, null, [3], null, null, null, null, null, null, [3], null, null, null, null, null, null, null, null, null, null, null, null, null], [null, [0], [0], [0], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null], [null, null, [0], [0], [0], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null], [null, null, null, [0], [0], [0], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null], [null, null, null, null, [0], [0], [0, 1], null, null, null, null, null, null, [1], null, null, null, null, null, null, [1], null, null, null, null, null, null, null], [null, null, null, null, null, [1, 0], [1, 0], null, null, null, null, null, [1], [1], null, null, null, null, null, [1], [1], null, null, null, null, null, null, null], [null, null, null, null, null, null, null, [3], [3], null, null, null, null, null, [3], [3], null, null, null, null, null, [3, 2], [3, 2], null, null, null, null, null], [null, null, null, null, null, null, null, [3], null, null, null, null, null, null, [3], null, null, null, null, null, null, [2, 3], [2], [2], null, null, null, null], [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [2], [2], [2], null, null, null], [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [2], [2], [2], null, null], [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [2], [2], [2], null], [null, null, null, null, null, null, null, null, null, null, null, null, null, [1], null, null, null, null, null, null, [1], null, null, null, null, [2], [2], [1, 2]], [null, null, null, null, null, null, null, null, null, null, null, null, [1], [1], null, null, null, null, null, [1], [1], null, null, null, null, null, [1, 2], [1, 2]], [null, null, null, null, null, null, null, null, null, null, null, null, null, null, [2, 3], [2, 3], null, null, null, null, null, [2, 3], [2, 3], null, null, null, null, null], [null, null, null, null, null, null, null, null, null, null, null, null, null, null, [2, 3], [2], [2], null, null, null, null, [2, 3], [2], [2], null, null, null, null], [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [2], [2], [2], null, null, null, null, [2], [2], [2], null, null, null], [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [2], [2], [2], null, null, null, null, [2], [2], [2], null, null], [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [2], [2], [2], null, null, null, null, [2], [2], [2], null], [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [2], [2], [2, 1], null, null, null, null, [2], [2], [2, 1]], [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [1, 2], [1, 2], null, null, null, null, null, [1, 2], [1, 2]]]
    };
    MnNneL[4] = {
        jAnOai: 45,
        BNECAi: [[1010000, 2830000], [16990000, 7170000]],
        FgAmGe: [[5990000, 5490000], [12010000, 7170000]],
        kEKLHa: [[9000000, 5480000], [10190000, 5480000]],
        IimcEf: {
            _1: [980000, 980000],
            _2: [980000, 9020000],
            _3: [17020000, 980000],
            _4: [17020000, 9020000]
        },
        ekbEHn: {
            _1: [635000, 635000],
            _3: [17365000, 635000],
            _4: [17365000, 9365000],
            _2: [635000, 9365000]
        },
        Imlbnm: [[1000000, 1280000, 0, -70000, 20000, 44400000000, 72801.09889280518], [980000, 1210000, 0, -270000, 270000, -62100000000, 381837.66184073564], [710000, 940000, 1, -230000, -230000, 379500000000, 325269.11934581184], [940000, 710000, 0, 270000, -270000, -62100000000, 381837.66184073564], [1210000, 980000, 0, 20000, -70000, 44400000000, 72801.09889280518], [1280000, 1000000, 0, 0, -2900000, 2900000000000, 2900000], [4180000, 1000000, 0, 1800000, -1800000, -5724000000000, 2545584.412271571], [5980000, 2800000, 0, 0, -6040000, 16912000000000, 6040000], [12020000, 2800000, 0, -1800000, -1800000, 26676000000000, 2545584.412271571], [13820000, 1000000, 0, 0, -2900000, 2900000000000, 2900000], [16720000, 1000000, 0, -20000, -70000, 404400000000, 72801.09889280518], [16790000, 980000, 0, -270000, -270000, 4797900000000, 381837.66184073564], [17060000, 710000, 3, 230000, -230000, -3760500000000, 325269.11934581184], [17290000, 940000, 0, 270000, 270000, -4922100000000, 381837.66184073564], [17020000, 1210000, 0, 70000, 20000, -1215600000000, 72801.09889280518], [17000000, 1280000, 0, 7440000, 0, -126480000000000, 7440000], [17000000, 8720000, 0, 70000, -20000, -1015600000000, 72801.09889280518], [17020000, 8790000, 0, 270000, -270000, -2222100000000, 381837.66184073564], [17290000, 9060000, 4, 230000, 230000, -6060500000000, 325269.11934581184], [17060000, 9290000, 0, -270000, 270000, 2097900000000, 381837.66184073564], [16790000, 9020000, 0, -20000, 70000, -295600000000, 72801.09889280518], [16720000, 9000000, 0, 0, 2900000, -26100000000000, 2900000], [13820000, 9000000, 0, -1800000, 1800000, 8676000000000, 2545584.412271571], [12020000, 7200000, 0, 0, 6040000, -43488000000000, 6040000], [5980000, 7200000, 0, 1800000, 1800000, -23724000000000, 2545584.412271571], [4180000, 9000000, 0, 0, 2900000, -26100000000000, 2900000], [1280000, 9000000, 0, 20000, 70000, -655600000000, 72801.09889280518], [1210000, 9020000, 0, 270000, 270000, -2762100000000, 381837.66184073564], [940000, 9290000, 2, -230000, 230000, -1920500000000, 325269.11934581184], [710000, 9060000, 0, -270000, -270000, 2637900000000, 381837.66184073564], [980000, 8790000, 0, -70000, -20000, 244400000000, 72801.09889280518], [1000000, 8720000, 0, -7440000, 0, 7440000000000, 7440000], [1000000, 1280000, 0]],
        JHiMkK: [[[0, 1, 2, 3, 4, 5, 31], [0, 1, 2, 3, 4, 5, 31, 6], null, null, null, null, null, [0, 1, 2, 3, 4, 5, 31], [0, 1, 2, 3, 4, 5, 31], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null], [[5, 6, 0, 1, 2, 3, 4, 31], [5, 6], [5, 6], null, null, null, null, [5, 6, 31], [5, 6], [5, 6, 7], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null], [null, [6, 5], [6], [6], null, null, null, null, [6], [6, 7], [6, 7], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null], [null, null, [6], null, [8], null, null, null, null, [6, 7], [7], [7, 8], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null], [null, null, null, [8], [8], [8, 9], null, null, null, null, [8, 7], [8, 7], [8], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null], [null, null, null, null, [8, 9], [8, 9], [8, 9, 10, 11, 12, 13, 14, 15], null, null, null, null, [8, 9, 7], [8, 9], [8, 9, 15], null, null, null, null, null, null, null, null, null, null, null, null, null, null], [null, null, null, null, null, [9, 10, 11, 12, 13, 14, 15, 8], [9, 10, 11, 12, 13, 14, 15], null, null, null, null, null, [9, 10, 11, 12, 13, 14, 15], [9, 10, 11, 12, 13, 14, 15], null, null, null, null, null, null, null, null, null, null, null, null, null, null], [[31, 0, 1, 2, 3, 4, 5], [31, 5, 6], null, null, null, null, null, [31], [31], null, null, null, null, null, [31], [31], null, null, null, null, null, null, null, null, null, null, null, null], [[0, 1, 2, 3, 4, 5, 31], [5, 6], [6], null, null, null, null, [31], null, [6, 7], null, null, null, null, [31], null, [23, 24], null, null, null, null, null, null, null, null, null, null, null], [null, [6, 7, 5], [6, 7], [6, 7], null, null, null, null, [6, 7], [6, 7], [6, 7], null, null, null, null, [6, 7], [6, 7, 23, 24], [6, 7, 23], null, null, null, null, null, null, null, null, null, null], [null, null, [7, 6], [7], [7, 8], null, null, null, null, [7, 6], [7], [7, 8], null, null, null, null, [7, 23, 24], [7, 23], [7, 22, 23], null, null, null, null, null, null, null, null, null], [null, null, null, [7, 8], [7, 8], [7, 8, 9], null, null, null, null, [7, 8], [7, 8], [7, 8], null, null, null, null, [7, 8, 23], [7, 8, 22, 23], [7, 8], null, null, null, null, null, null, null, null], [null, null, null, null, [8], [8, 9], [9, 10, 11, 12, 13, 14, 15], null, null, null, null, [7, 8], null, [15], null, null, null, null, [22, 23], null, [15], null, null, null, null, null, null, null], [null, null, null, null, null, [15, 8, 9], [15, 9, 10, 11, 12, 13, 14], null, null, null, null, null, [15], [15], null, null, null, null, null, [15], [15], null, null, null, null, null, null, null], [null, null, null, null, null, null, null, [31], [31], null, null, null, null, null, [31], [31], null, null, null, null, null, [31, 25, 26, 27, 28, 29, 30], [31, 24, 25], null, null, null, null, null], [null, null, null, null, null, null, null, [31], null, [6, 7], null, null, null, null, [31], null, [23, 24], null, null, null, null, [25, 26, 27, 28, 29, 30, 31], [24, 25], [24], null, null, null, null], [null, null, null, null, null, null, null, null, [23, 24], [23, 24, 6, 7], [23, 24, 7], null, null, null, null, [23, 24], [23, 24], [23, 24], null, null, null, null, [23, 24, 25], [23, 24], [23, 24], null, null, null], [null, null, null, null, null, null, null, null, null, [23, 6, 7], [23, 7], [23, 7, 8], null, null, null, null, [23, 24], [23], [23, 22], null, null, null, null, [23, 24], [23], [23, 22], null, null], [null, null, null, null, null, null, null, null, null, null, [22, 23, 7], [22, 23, 7, 8], [22, 23], null, null, null, null, [22, 23], [22, 23], [22, 23], null, null, null, null, [22, 23], [22, 23], [22, 23, 21], null], [null, null, null, null, null, null, null, null, null, null, null, [7, 8], null, [15], null, null, null, null, [22, 23], null, [15], null, null, null, null, [22], [21, 22], [15, 16, 17, 18, 19, 20, 21]], [null, null, null, null, null, null, null, null, null, null, null, null, [15], [15], null, null, null, null, null, [15], [15], null, null, null, null, null, [15, 21, 22], [15, 16, 17, 18, 19, 20, 21]], [null, null, null, null, null, null, null, null, null, null, null, null, null, null, [25, 26, 27, 28, 29, 30, 31], [25, 26, 27, 28, 29, 30, 31], null, null, null, null, null, [25, 26, 27, 28, 29, 30, 31], [25, 26, 27, 28, 29, 30, 31, 24], null, null, null, null, null], [null, null, null, null, null, null, null, null, null, null, null, null, null, null, [24, 25, 31], [24, 25], [24, 25, 23], null, null, null, null, [24, 25, 26, 27, 28, 29, 30, 31], [24, 25], [24, 25], null, null, null, null], [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [24], [24, 23], [24, 23], null, null, null, null, [24, 25], [24], [24], null, null, null], [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [23, 24], [23], [22, 23], null, null, null, null, [24], null, [22], null, null], [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [22, 23], [22, 23], [22], null, null, null, null, [22], [22], [22, 21], null], [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [21, 22, 23], [21, 22], [21, 22, 15], null, null, null, null, [21, 22], [21, 22], [21, 22, 15, 16, 17, 18, 19, 20]], [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [15, 16, 17, 18, 19, 20, 21], [15, 16, 17, 18, 19, 20, 21], null, null, null, null, null, [15, 16, 17, 18, 19, 20, 21, 22], [15, 16, 17, 18, 19, 20, 21]]]
    };
    MnNneL[5] = {
        jAnOai: 45,
        BNECAi: [[980000, 980000], [17020000, 9020000]],
        FgAmGe: [[13130000, 980000], [17020000, 9020000]],
        kEKLHa: [[13120000, 5000000], [13120000, 3420000]],
        IimcEf: {
            _1: [970000, 970000],
            _2: [970000, 9030000],
            _3: [9000000, 750000],
            _4: [9000000, 9250000],
            _5: [17030000, 970000],
            _6: [17030000, 9030000]
        },
        ekbEHn: {
            _1: [620000, 620000],
            _3: [9000000, 480000],
            _5: [17380000, 620000],
            _6: [17380000, 9380000],
            _4: [9000000, 9520000],
            _2: [620000, 9380000]
        },
        Imlbnm: [[970000, 1250000, 0, -50000, 10000, 36000000000, 50990.19513592785], [960000, 1200000, 0, -280000, 250000, -31200000000, 375366.4875824692], [710000, 920000, 1, -210000, -210000, 342300000000, 296984.84809834993], [920000, 710000, 0, 250000, -280000, -31200000000, 375366.4875824692], [1200000, 960000, 0, 10000, -50000, 36000000000, 50990.19513592785], [1250000, 970000, 0, 0, -7380000, 7158600000000, 7380000], [8630000, 970000, 0, -30000, -60000, 317100000000, 67082.03932499369], [8690000, 940000, 0, -260000, -140000, 2391000000000, 295296.461204668], [8830000, 680000, 3, 0, -340000, 231200000000, 340000], [9170000, 680000, 0, 260000, -140000, -2289000000000, 295296.461204668], [9310000, 940000, 0, 30000, -60000, -222900000000, 67082.03932499369], [9370000, 970000, 0, 0, -7380000, 7158600000000, 7380000], [16750000, 970000, 0, -10000, -50000, 216000000000, 50990.19513592785], [16800000, 960000, 0, -250000, -280000, 4468800000000, 375366.4875824692], [17080000, 710000, 5, 210000, -210000, -3437700000000, 296984.84809834993], [17290000, 920000, 0, 280000, 250000, -5071200000000, 375366.4875824692], [17040000, 1200000, 0, 50000, 10000, -864000000000, 50990.19513592785], [17030000, 1250000, 0, 7500000, 0, -127725000000000, 7500000], [17030000, 8750000, 0, 50000, -10000, -764000000000, 50990.19513592785], [17040000, 8800000, 0, 280000, -250000, -2571200000000, 375366.4875824692], [17290000, 9080000, 6, 210000, 210000, -5537700000000, 296984.84809834993], [17080000, 9290000, 0, -250000, 280000, 1668800000000, 375366.4875824692], [16800000, 9040000, 0, -10000, 50000, -284000000000, 50990.19513592785], [16750000, 9030000, 0, 0, 7380000, -66641400000000, 7380000], [9370000, 9030000, 0, 30000, 60000, -822900000000, 67082.03932499369], [9310000, 9060000, 0, 260000, 140000, -3689000000000, 295296.461204668], [9170000, 9320000, 4, 0, 340000, -3168800000000, 340000], [8830000, 9320000, 0, -260000, 140000, 991000000000, 295296.461204668], [8690000, 9060000, 0, -30000, 60000, -282900000000, 67082.03932499369], [8630000, 9030000, 0, 0, 7380000, -66641400000000, 7380000], [1250000, 9030000, 0, 10000, 50000, -464000000000, 50990.19513592785], [1200000, 9040000, 0, 250000, 280000, -2831200000000, 375366.4875824692], [920000, 9290000, 2, -210000, 210000, -1757700000000, 296984.84809834993], [710000, 9080000, 0, -280000, -250000, 2468800000000, 375366.4875824692], [960000, 8800000, 0, -50000, -10000, 136000000000, 50990.19513592785], [970000, 8750000, 0, -7500000, 0, 7275000000000, 7500000], [970000, 1250000, 0]],
        JHiMkK: [[[0, 1, 2, 3, 4, 5, 35], [0, 1, 2, 3, 4, 5, 35], null, null, null, null, null, [0, 1, 2, 3, 4, 5, 35], [0, 1, 2, 3, 4, 5, 35], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null], [[5, 0, 1, 2, 3, 4, 35], [5], [5], null, null, null, null, [5, 35], [5], [5], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null], [null, [5], [5], [5, 6, 7, 8, 9, 10, 11], null, null, null, null, [5], [5], [5], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null], [null, null, [5, 6, 7, 8, 9, 10, 11], [5, 6, 7, 8, 9, 10, 11], [5, 6, 7, 8, 9, 10, 11], null, null, null, null, [5, 6, 7, 8, 9, 10, 11], [5, 6, 7, 8, 9, 10, 11], [5, 6, 7, 8, 9, 10, 11], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null], [null, null, null, [11, 5, 6, 7, 8, 9, 10], [11], [11], null, null, null, null, [11], [11], [11], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null], [null, null, null, null, [11], [11], [11, 12, 13, 14, 15, 16, 17], null, null, null, null, [11], [11], [11, 17], null, null, null, null, null, null, null, null, null, null, null, null, null, null], [null, null, null, null, null, [11, 12, 13, 14, 15, 16, 17], [11, 12, 13, 14, 15, 16, 17], null, null, null, null, null, [11, 12, 13, 14, 15, 16, 17], [11, 12, 13, 14, 15, 16, 17], null, null, null, null, null, null, null, null, null, null, null, null, null, null], [[35, 0, 1, 2, 3, 4, 5], [35, 5], null, null, null, null, null, [35], [35], null, null, null, null, null, [35], [35], null, null, null, null, null, null, null, null, null, null, null, null], [[0, 1, 2, 3, 4, 5, 35], [5], [5], null, null, null, null, [35], null, null, null, null, null, null, [35], null, null, null, null, null, null, null, null, null, null, null, null, null], [null, [5], [5], [5, 6, 7, 8, 9, 10, 11], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null], [null, null, [5], [5, 6, 7, 8, 9, 10, 11], [11], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null], [null, null, null, [5, 6, 7, 8, 9, 10, 11], [11], [11], null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null], [null, null, null, null, [11], [11], [11, 12, 13, 14, 15, 16, 17], null, null, null, null, null, null, [17], null, null, null, null, null, null, [17], null, null, null, null, null, null, null], [null, null, null, null, null, [17, 11], [17, 11, 12, 13, 14, 15, 16], null, null, null, null, null, [17], [17], null, null, null, null, null, [17], [17], null, null, null, null, null, null, null], [null, null, null, null, null, null, null, [35], [35], null, null, null, null, null, [35], [35], null, null, null, null, null, [35, 29, 30, 31, 32, 33, 34], [35, 29], null, null, null, null, null], [null, null, null, null, null, null, null, [35], null, null, null, null, null, null, [35], null, null, null, null, null, null, [29, 30, 31, 32, 33, 34, 35], [29], [29], null, null, null, null], [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [29], [29], [23, 24, 25, 26, 27, 28, 29], null, null, null], [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [29], [23, 24, 25, 26, 27, 28, 29], [23], null, null], [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [23, 24, 25, 26, 27, 28, 29], [23], [23], null], [null, null, null, null, null, null, null, null, null, null, null, null, null, [17], null, null, null, null, null, null, [17], null, null, null, null, [23], [23], [17, 18, 19, 20, 21, 22, 23]], [null, null, null, null, null, null, null, null, null, null, null, null, [17], [17], null, null, null, null, null, [17], [17], null, null, null, null, null, [17, 23], [17, 18, 19, 20, 21, 22, 23]], [null, null, null, null, null, null, null, null, null, null, null, null, null, null, [29, 30, 31, 32, 33, 34, 35], [29, 30, 31, 32, 33, 34, 35], null, null, null, null, null, [29, 30, 31, 32, 33, 34, 35], [29, 30, 31, 32, 33, 34, 35], null, null, null, null, null], [null, null, null, null, null, null, null, null, null, null, null, null, null, null, [29, 35], [29], [29], null, null, null, null, [29, 30, 31, 32, 33, 34, 35], [29], [29], null, null, null, null], [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [29], [29], [29], null, null, null, null, [29], [29], [29, 23, 24, 25, 26, 27, 28], null, null, null], [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [23, 24, 25, 26, 27, 28, 29], [23, 24, 25, 26, 27, 28, 29], [23, 24, 25, 26, 27, 28, 29], null, null, null, null, [23, 24, 25, 26, 27, 28, 29], [23, 24, 25, 26, 27, 28, 29], [23, 24, 25, 26, 27, 28, 29], null, null], [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [23], [23], [23], null, null, null, null, [23, 24, 25, 26, 27, 28, 29], [23], [23], null], [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [23], [23], [23, 17], null, null, null, null, [23], [23], [23, 17, 18, 19, 20, 21, 22]], [null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, [17, 18, 19, 20, 21, 22, 23], [17, 18, 19, 20, 21, 22, 23], null, null, null, null, null, [17, 18, 19, 20, 21, 22, 23], [17, 18, 19, 20, 21, 22, 23]]]
    };
    var LIKAgg, NgjbIn, amlClm, MEaoDC, eLAKFi, FdDBNA, oIieDj, EPJHkf;
    var mhlkef, beBjbj, FcooBM, CJHGCK, NOAbGk, fLoOmD;
    var EDdliE, bJefno, Nhgpna, hFNgFN, kmHOGk;
    var OdjMli, GIgPag, KmkHIm, lKclNn, dgcnik, bgLEIF, fBfhIC, jGhjGb, AapNgp, HnPGCc;
    var OOfOEh, imfodK, kcJokA, cCJPfc, pdOcjk, heOOOB, danOlm, PAHapA, mFcNma, nfGFPn, angnGb, kOPFmM, KhnHoD;
    var hHgcCD, NdGnPG, HkAGdB, cnoMOg, OdpkmM, lBlIhb, IedkAJ, ipgmHM, podbCd, EObkea, PoeeGO;
    var eAeFAO = function (jCEMkN) {
        var AfekcP = jCEMkN;
        jCEMkN.eAeFAO = this;
        this.LcJlao = 0;
        this.jHIGoB = false;
        this.kIHhDL = false;
        this.oLnMib = true;
        this.hJJlNP = true;
        this.NoCccJ = 1;
        this.FmOnAi = function (PeejaG, eCcOkf, CjncJN) {
            return AfekcP.FmOnAi(PeejaG, eCcOkf, CjncJN);
        };
        this.kiPEEd = function () {
            AfekcP.kiPEEd();
        };
        this.KDJcda = function (MlomAd) {
            AfekcP.KDJcda(MlomAd);
        };
        this.hIFbom = function () {
            AfekcP.hIFbom();
        };
        this.jpAJGd = function () {
            AfekcP.jpAJGd();
        };
        this.MchKjg = function () {
            AfekcP.MchKjg();
        };
        this.jJNMeA = function (HLkCLj) {
            AfekcP.jJNMeA(HLkCLj);
        };
        this.ccMhlO = function (ANFEbB) {
            AfekcP.ccMhlO(ANFEbB);
        };
        this.loNDBD = function (CGnGMk) {
            AfekcP.loNDBD(CGnGMk);
        };
        this.iDGbPe = function (PDipmG) {
            AfekcP.iDGbPe(PDipmG);
        };
        this.FMGaPH = function (KEjEEl) {
            return AfekcP.FMGaPH(KEjEEl);
        };
        this.nbgJof = function (KEjEEl) {
            return AfekcP.nbgJof(KEjEEl);
        };
        this.DhcNbm = function (KEjEEl) {
            return AfekcP.DhcNbm(KEjEEl);
        };
    };
    var JpMdFf = function (lIomEJ) {
        this.fkpbbL(lIomEJ);
    };
    JpMdFf.prototype.fkpbbL = function (lIomEJ) {
        if (lIomEJ.length < 2) {
            $error(20819591);
            return;
        };
        if (this.AIIHhG) {
            $error(20819592);
            return;
        };
        if (!EEJefK(lIomEJ[0])) {
            $error(20819593);
            return;
        };
        if (lIomEJ[1]) {
            ilhJLf = 1;
        } else {
            ilhJLf = 0;
        };
        this.eAeFAO = null;
        this.jJIAdD = BLAZE.nhjLnH.fnKEDK();
        this.hBeflg = false;
        this.gnaGcc();
        this.AIIHhG = lIomEJ[0];
        this.Biabka = null;
        this.bDnigP = null;
        this.aaPLhk = null;
        this.BkoHcI = null;
        this.MCaChp = null;
        this.CipCaF = new BLAZE.EejcjF('BilliardsRenderer', mKEgAF[0], mKEgAF[1], 1, ilhJLf);
        this.CipCaF.acfdaJ = true;
        this.CipCaF.KdieCl = false;
        this.CipCaF.IPPmOm = false;
        this.CipCaF.IgMlEF.CClMcd = true;
        this.JgOAFb = BLAZE.nhjLnH.oAclpm('element', 'game.billiards_cue');
        if (!this.JgOAFb) {
            $error(68377191);
            return;
        };
        ggGkJc.ikDpkl(this.JgOAFb);
        this.iNbfnE = this.JgOAFb.FeKiLh.container;
        this.EJeBcH = this.JgOAFb.FeKiLh.source;
        this.JNGiGP = this.JgOAFb.FeKiLh.anim;
        if (!this.iNbfnE || !this.EJeBcH || !this.JNGiGP) {
            $error(68377192);
            return;
        };
        this.LcdpGp = BLAZE.nhjLnH.oAclpm('element', 'game.billiards_table');
        if (!this.LcdpGp) {
            $error(63950928);
            return;
        };
        ggGkJc.ikDpkl(this.LcdpGp);
        this.LcdpGp.KJkiNL = true;
        this.CPIOma = BLAZE.nhjLnH.oAclpm('element', 'game.billiards_effect_foreground');
        if (!this.CPIOma) {
            $error(59039921);
            return;
        };
        this.eliJhL = BLAZE.nhjLnH.oAclpm('element', 'game.billiards_effect_background');
        if (!this.eliJhL) {
            $error(59683746);
            return;
        };
        ggGkJc.ikDpkl(this.CPIOma);
        ggGkJc.ikDpkl(this.eliJhL);
        this.aadigp = BLAZE.nhjLnH.oAclpm('element', 'game.billiards_guide');
        if (!this.aadigp) {
            $error(11927504);
            return;
        };
        ggGkJc.ikDpkl(this.aadigp);
        this.DKElck = this.aadigp.FeKiLh.start;
        this.PbbfcC = this.aadigp.FeKiLh.start_line;
        this.FpMEcj = this.aadigp.FeKiLh.end;
        this.KLGIdh = this.aadigp.FeKiLh.end_line;
        this.OcgFdh = this.aadigp.FeKiLh.collider;
        this.GLcnGe = this.aadigp.FeKiLh.collider_line;
        this.MCaChp = BLAZE.nhjLnH.oAclpm('element', 'game.billiards_place_ball');
        if (!this.MCaChp) {
            $error(49862271);
            return;
        };
        ggGkJc.ikDpkl(this.MCaChp);
        this.MCaChp.FmfGpK = true;
        this.MCaChp.MlomAd = null;
        this.MCaChp.NLedNa = false;
        this.MCaChp.classList.remove('deny');
        this.MCaChp.AcPOPM = [0, 0];
        this.gdceHj = BLAZE.nhjLnH.oAclpm('element', 'game.billiards_spin_menu');
        if (!this.gdceHj) {
            $error(94870278);
            return;
        };
        ggGkJc.ikDpkl(this.gdceHj);
        var GmbpEk = this;
        this.dIHJno = function (fMnbiD) {
            GmbpEk.DHpnNm(fMnbiD);
        };
        this.dKHaJL = function (fMnbiD) {
            GmbpEk.AHgKJg(fMnbiD);
        };
        this.GGAbhE = function (fMnbiD) {
            GmbpEk.khPphk(fMnbiD);
        };
        this.Mdbadf = function (fMnbiD) {
            GmbpEk.pacHco(fMnbiD);
        };
        this.kEkfAm = function (fMnbiD) {
            GmbpEk.cHBChG(fMnbiD);
        };
        this.ffDheh = function (fMnbiD) {
            GmbpEk.LDLgJP(fMnbiD);
        };
        this.LDllAF = function (fMnbiD) {
            GmbpEk.lkkAbJ(fMnbiD);
        };
        this.pnCNpp = function (fMnbiD) {
            GmbpEk.CllplA(fMnbiD);
        };
        this.ipnmGC = function (fMnbiD) {
            GmbpEk.FLJegn(fMnbiD);
        };
        this.feFPnD = function (fMnbiD) {
            GmbpEk.GmAfbE(fMnbiD);
        };
        this.COfAbn = function (fMnbiD) {
            GmbpEk.cdfANN(fMnbiD);
        }
    };
    JpMdFf.prototype.FmOnAi = function (PeejaG, eCcOkf, CjncJN) {
        if (!this.AIIHhG) {
            $warn(2290681);
            return false;
        };
        if (this.hBeflg) {
            $warn(2290682);
            return false;
        };
        if (!PeejaG) {
            $warn(2290683);
            return false;
        };
        if (!eCcOkf) {
            $warn(2290684);
            return false;
        };
        var DnMOJK = 0;
        if (CjncJN) {
            DnMOJK = 1;
        };
        if (ilhJLf != DnMOJK) {
            ilhJLf = DnMOJK;
            this.CipCaF.nbpblG();
            this.CipCaF.jNdIig();
            this.CipCaF = new BLAZE.EejcjF('BilliardsRenderer', mKEgAF[0], mKEgAF[1], 1, ilhJLf);
            this.CipCaF.acfdaJ = true;
            this.CipCaF.KdieCl = false;
            this.CipCaF.IPPmOm = false;
            this.CipCaF.IgMlEF.CClMcd = true;
        };
        this.gnaGcc();
        if (eCcOkf.length != 11) {
            $warn(64223638);
            return false;
        };
        eCcOkf[2] = NmbiKM(eCcOkf[2]);
        eCcOkf[3] = NmbiKM(eCcOkf[3]);
        eCcOkf[4] = NmbiKM(eCcOkf[4]);
        eCcOkf[5] = NmbiKM(eCcOkf[5]);
        eCcOkf[6] = NmbiKM(eCcOkf[6]);
        eCcOkf[7] = NmbiKM(eCcOkf[7]);
        this.BJoBNk = eCcOkf;
        this.lKGHhh = eCcOkf[5] == 1;
        this.ebkjkE = eCcOkf[6] == 1;
        this.oackNC('standard', BLAZE.nhjLnH.oAclpm('bitmap', 'billiards_default_cue'), this);
        this.Biabka = PeejaG;
        var FeKiLh = this.Biabka.FeKiLh;
        this.OlGPmN = PeejaG.parentNode;
        if (!this.OlGPmN) {
            $error(95882103);
            return;
        };
        this.KcMlaa = ggGkJc.oAcDfp(this.OlGPmN);
        this.bDnigP = FeKiLh.GameScoreboard;
        this.aaPLhk = FeKiLh.GameArea;
        this.lBFeil = FeKiLh.GameFullZone;
        this.BkoHcI = FeKiLh.GameTable;
        this.LcdpGp.FeKiLh.table_super_game.classList.remove('AnimSuperGame');
        this.BkoHcI.appendChild(this.LcdpGp);
        this.BkoHcI.appendChild(this.eliJhL);
        this.CipCaF.bGanCM(this.BkoHcI);
        this.BkoHcI.appendChild(this.CPIOma);
        this.BkoHcI.appendChild(this.aadigp);
        this.LoELbN = ggGkJc.oAcDfp(this.aadigp);
        this.MCaChp.MlomAd = null;
        this.MCaChp.NLedNa = false;
        this.MCaChp.classList.remove('deny');
        this.MCaChp.AcPOPM = [0, 0];
        this.AIIHhG.ojJMoF(mKEgAF, true);
        this.LcdpGp.addEventListener('mousedown', this.dIHJno, false);
        this.lBFeil.addEventListener('mousedown', this.dIHJno, false);
        document.addEventListener('mouseup', this.dKHaJL, true);
        document.addEventListener('mousemove', this.GGAbhE, true);
        this.LcdpGp.addEventListener('touchstart', this.Mdbadf, false);
        document.addEventListener('touchend', this.kEkfAm, true);
        document.addEventListener('touchcancel', this.ffDheh, true);
        document.addEventListener('touchmove', this.LDllAF, true);
        this.Biabka.addEventListener('touchmove', this.pnCNpp, false);
        this.gdceHj.addEventListener('mouseleave', this.ipnmGC, false);
        this.gdceHj.addEventListener('mousedown', this.feFPnD, false);
        this.gdceHj.addEventListener('touchstart', this.COfAbn, false);
        this.iIKgJL(eCcOkf[7], eCcOkf[8], eCcOkf[9], eCcOkf[10], 0);
        this.hBeflg = true;
        this.iEJHDn(0);
        BLAZE.bacjNj.hfJPGI(this, this.CipCaF);
        return true;
    };
    JpMdFf.prototype.kiPEEd = function () {
        if (!this.AIIHhG) {
            $warn(59029918);
            return;
        };
        BLAZE.bacjNj.eJNGli();
        this.iEJHDn(0);
        this.inoPPG();
        this.DJafbE();
        this.ojjAHN();
        this.gnaGcc();
        this.hBeflg = false;
        if (this.Biabka) {
            this.Biabka.removeEventListener('touchmove', this.pnCNpp, false);
        };
        if (this.LcdpGp) {
            this.LcdpGp.removeEventListener('mousedown', this.dIHJno, false);
            this.lBFeil.removeEventListener('mousedown', this.dIHJno, false);
            document.removeEventListener('mouseup', this.dKHaJL, true);
            document.removeEventListener('mousemove', this.GGAbhE, true);
            this.LcdpGp.removeEventListener('touchstart', this.Mdbadf, false);
            document.removeEventListener('touchend', this.kEkfAm, true);
            document.removeEventListener('touchcancel', this.ffDheh, true);
            document.removeEventListener('touchmove', this.LDllAF, true);
            if (this.LcdpGp.parentNode) {
                this.LcdpGp.parentNode.removeChild(this.LcdpGp);
            };
            this.LcdpGp.FeKiLh.table_super_game.classList.remove('AnimSuperGame');
        };
        if (this.gdceHj) {
            this.gdceHj.removeEventListener('mouseleave', this.ipnmGC, false);
            this.gdceHj.removeEventListener('mousedown', this.feFPnD, false);
            this.gdceHj.removeEventListener('touchstart', this.COfAbn, false);
        };
        if (this.aadigp) {
            if (this.aadigp.parentNode) {
                this.aadigp.parentNode.removeChild(this.aadigp);
            }
        };
        if (this.CPIOma) {
            if (this.CPIOma.parentNode) {
                this.CPIOma.parentNode.removeChild(this.CPIOma);
            }
        };
        if (this.eliJhL) {
            if (this.eliJhL.parentNode) {
                this.eliJhL.parentNode.removeChild(this.eliJhL);
            }
        };
        if (this.CipCaF) {
            this.CipCaF.jNdIig();
            this.CipCaF.pAKJck();
        };
        if (this.JgOAFb) {
            if (this.JgOAFb.parentNode) {
                this.JgOAFb.parentNode.removeChild(this.JgOAFb);
            }
        };
        this.Biabka = null;
        this.bDnigP = null;
        this.aaPLhk = null;
        this.BkoHcI = null;
    };
    JpMdFf.prototype.MchKjg = function () {
        this.kiPEEd();
        this.AIIHhG = null;
        this.LcdpGp = null;
        this.aadigp = null;
        this.CPIOma = null;
        this.eliJhL = null;
        this.CipCaF = null;
        this.MCaChp = null;
        this.gdceHj = null;
        this.JgOAFb = null;
        this.iNbfnE = null;
        this.EJeBcH = null;
        hkdcJB.EopacH(this.JNGiGP, true);
        this.JNGiGP = null;
        this.DKElck = null;
        this.PbbfcC = null;
        this.FpMEcj = null;
        this.KLGIdh = null;
        this.OcgFdh = null;
        this.GLcnGe = null;
    };
    JpMdFf.prototype.gnaGcc = function () {
        this.dCLkjM = null;
        this.eLHmnH = false;
        this.LlCjig = 0;
        this.ImnNgj = '';
        this.BJoBNk = null;
        this.lKGHhh = false;
        this.ebkjkE = false;
        this.CnokOK = [];
        this.BidDIf = [];
        this.FLJHLb = null;
        this.NAdBAN = null;
        this.GJCkgG = 1.0;
        this.bglKFc = 0;
        this.pnkKjh = 0;
        this.ocFimm = 0;
        this.pPCABE = 0;
        this.OfbJPI = 0;
        this.ICNDka = 0;
        this.DONAgB = null;
        this.ebDANl = null;
        this.LECdmi = null;
        this.bHBDje = null;
        this.lMfbLD = null;
        this.hacgoO = 0;
        this.oJPEMN = 0;
        this.NmmCpf = 0;
        this.oKpmDB = 0;
        this.lPColI = '';
        this.FNNEFK = [0, 0];
        this.AFmPcM = [0, 0];
        this.oGjpOo = [0, 0];
        this.dodcjj = 0;
        this.BKMLoe = 0;
        this.OhJEbo = afLliH;
        this.maIOaI = 0;
        this.BdimnP = false;
        this.IcjAkH = 0;
        this.lLDEmb = 0;
        this.gAhNem = {};
        this.JefDNA = [0, 0];
        this.pKfEKp = false;
        this.KEMAdJ = [0, 0];
        this.CGLcbM = -1;
        this.GLJCMC = 0;
        this.eAAjjm = 0;
        this.GndaMA = 0;
        this.GFcFhe = 0;
        this.gFednf = false;
        this.JENiKa = false;
        this.mEpLnC = null;
        this.nDIkHO = false;
        this.fghCeo = null;
        this.FFaNCh = null;
        this.GeBcJp = null;
        this.dPOkmj = [];
        this.DgGcoe = [];
        if (this.DKElck) {
            this.DKElck.style.display = 'none';
        };
        if (this.FpMEcj) {
            this.FpMEcj.style.display = 'none';
        };
        if (this.OcgFdh) {
            this.OcgFdh.style.display = 'none';
        };
        this.aeIOMF = -1;
        this.KKmlPp = 0;
        this.jMpMAo = 0;
        this.pPGclC = [];
        this.njMdfO = {};
        this.cnaFhk = false;
    };
    JpMdFf.prototype.ccMhlO = function (ANFEbB) {
        if (!this.hBeflg) {
            return;
        };
        if (this.LcdpGp) {
            var oeigjE = this.LcdpGp.FeKiLh;
            oeigjE.table_super_game_zp.innerHTML = ANFEbB + ' ZP';
            oeigjE.table_super_game.classList.add('AnimSuperGame');
        }
    };
    JpMdFf.prototype.iDGbPe = function (MpONGN) {
        if (!this.hBeflg) {
            return;
        };
        var MBllBn, DILNMg, PDipmG;
        this.KcMlaa = ggGkJc.oAcDfp(this.OlGPmN);
        this.LoELbN = ggGkJc.oAcDfp(this.aadigp);
        var OIgcNj = MpONGN[0] + 'px';
        var LapKCP = MpONGN[1] + 'px';
        this.GJCkgG = MpONGN[0] / mKEgAF[0];
        if (this.LcdpGp) {
            this.LcdpGp.style.width = OIgcNj;
            this.LcdpGp.style.height = LapKCP;
            var LIhgij = Math.round(this.ICNDka * this.GJCkgG) + 'px';
            MBllBn = this.LcdpGp.FeKiLh.table_markers.style;
            MBllBn.top = LIhgij;
            MBllBn.bottom = LIhgij;
            MBllBn.left = LIhgij;
            MBllBn.right = LIhgij;
            MBllBn = this.LcdpGp.FeKiLh.table_default_fabric.style;
            MBllBn.top = LIhgij;
            MBllBn.bottom = LIhgij;
            MBllBn.left = LIhgij;
            MBllBn.right = LIhgij;
            MBllBn = this.LcdpGp.FeKiLh.table_fabric.style;
            MBllBn.top = LIhgij;
            MBllBn.bottom = LIhgij;
            MBllBn.left = LIhgij;
            MBllBn.right = LIhgij;
            MBllBn = this.LcdpGp.FeKiLh.table_image.style;
            MBllBn.top = LIhgij;
            MBllBn.bottom = LIhgij;
            MBllBn.left = LIhgij;
            MBllBn.right = LIhgij;
        };
        if (this.CipCaF) {
            this.CipCaF.IgMlEF.style.width = OIgcNj;
            this.CipCaF.IgMlEF.style.height = LapKCP;
        };
        if (this.MCaChp) {
            if (this.MCaChp.MlomAd && this.MCaChp.parentNode && BLAZE.nhjLnH.lboAhk) {
                this.fIPaLb(this.MCaChp.MlomAd);
            } else {
                this.HDNDed(true, false);
            }
        };
        if (this.JgOAFb) {
            PDipmG = lJELmO.PAGKnH(EhBAol, this.GJCkgG);
            lJELmO.BObpdE(PDipmG);
            this.iNbfnE.style.width = PDipmG[0] + 'px';
            this.iNbfnE.style.height = PDipmG[1] + 'px';
            this.iNbfnE.style.left = (-Math.round(PDipmG[0] * 0.5)) + 'px';
            if (this.eAAjjm > 0) {
                lJELmO.cJJPaG(this.FNNEFK, this.AFmPcM);
                this.nbgJof(this.AFmPcM, this.OlGPmN);
                lJELmO.IFDeod(this.AFmPcM, this.KcMlaa);
                this.JgOAFb.style.left = this.AFmPcM[0] + 'px';
                this.JgOAFb.style.top = this.AFmPcM[1] + 'px';
                this.bKclpB();
                if (this.eAAjjm == 2) {
                    this.BdimnP = true;
                }
            };
        };
        if (this.fghCeo) {
            this.MOIged(this.fghCeo, this.nDIkHO);
        };
        if (this.FFaNCh) {
            this.KAGcGh(this.FFaNCh);
        };
        this.IHFOKF();
        this.laLjpB();
        this.HJgeKM();
        BLAZE.bacjNj.cDOgbJ(MpONGN, this.GJCkgG, this.NmmCpf);
    };
    JpMdFf.prototype.HDNDed = function (dMmjnA, CafOkf) {
        var DILNMg, HIhniL, MBllBn = this.MCaChp.style;
        if (dMmjnA) {
            var PDipmG = ogNmao;
            var ALaBhn = 0;
            if (CafOkf) {
                if (BLAZE.nhjLnH.lboAhk) {
                    ALaBhn = JfnKmi;
                }
            } else {
                if (BLAZE.nhjLnH.lboAhk) {
                    ALaBhn = JfOHAI;
                }
            };
            if (ALaBhn < this.GJCkgG) {
                ALaBhn = this.GJCkgG;
            };
            PDipmG = HAELdp.BObpdE(PDipmG * ALaBhn);
            DILNMg = PDipmG + 'px';
            MBllBn.width = DILNMg;
            MBllBn.height = DILNMg;
            DILNMg = HAELdp.BObpdE(PDipmG * -0.5) + 'px';
            MBllBn.margin = DILNMg + ' 0 0 ' + DILNMg;
        };
        if (!this.MCaChp.MlomAd) {
            return;
        };
        DILNMg = lJELmO.NoeNdn(this.MCaChp.AcPOPM);
        this.FMGaPH(DILNMg);
        if (this.jjMaaf(this.MCaChp.MlomAd[4], this.MCaChp.MlomAd[1], DILNMg)) {
            if (this.MCaChp.NLedNa) {
                this.MCaChp.NLedNa = false;
                this.MCaChp.classList.remove('deny');
            }
        } else {
            if (!this.MCaChp.NLedNa) {
                this.MCaChp.NLedNa = true;
                this.MCaChp.classList.add('deny');
            }
        };
        this.nbgJof(DILNMg);
        HIhniL = lJELmO.khOMcp(DILNMg, this.KcMlaa);
        MBllBn.left = HIhniL[0] + 'px';
        MBllBn.top = HIhniL[1] + 'px';
    };
    JpMdFf.prototype.fHepCk = function () {
        var MlomAd = this.MCaChp.MlomAd;
        if (!MlomAd) {
            return;
        };
        var DILNMg = lJELmO.NoeNdn(this.MCaChp.AcPOPM);
        this.FMGaPH(DILNMg);
        if (!this.jjMaaf(MlomAd[4], MlomAd[1], DILNMg)) {
            if (BLAZE.nhjLnH.lboAhk) {
                this.fIPaLb(MlomAd);
                this.HDNDed(true, false);
            };
            return;
        };
        this.inoPPG();
        var OPKHjd = this.kDBpDc(MlomAd[1]);
        if (!OPKHjd) {
            return;
        };
        lJELmO.cJJPaG(DILNMg, OPKHjd[2]);
        this.jMcjpd(OPKHjd);
        this.CipCaF.aGcIfL();
        this.AIIHhG.DJMNpK({
            c: 'plc',
            v: [OPKHjd[0], mPIIDJ.kNAikO(OPKHjd[2][0], 0), mPIIDJ.kNAikO(OPKHjd[2][1], 0)].join(':')
        });
        this.MDfoNP(MlomAd[1], MlomAd[2], MlomAd[3], false);
    };
    JpMdFf.prototype.BcLMBg = function () {
        if (!this.MCaChp.MlomAd) {
            return;
        };
        lJELmO.cJJPaG(this.JefDNA, this.MCaChp.AcPOPM);
        this.HDNDed(true, true);
    };
    JpMdFf.prototype.fIPaLb = function (MlomAd) {
        if (!MlomAd) {
            $warn(57990285);
            return;
        };
        MlomAd[1] = NmbiKM(MlomAd[1]);
        MlomAd[2] = NmbiKM(MlomAd[2]);
        MlomAd[3] = NmbiKM(MlomAd[3]);
        MlomAd[4] = NmbiKM(MlomAd[4]);
        if (this.MCaChp.NLedNa) {
            this.MCaChp.NLedNa = false;
            this.MCaChp.classList.remove('deny');
        };
        this.MCaChp.MlomAd = MlomAd;
        this.OlGPmN.appendChild(this.MCaChp);
        if (BLAZE.nhjLnH.lboAhk) {
            var OPKHjd = this.kDBpDc(MlomAd[1]);
            if (OPKHjd) {
                lJELmO.cJJPaG(OPKHjd[2], this.MCaChp.AcPOPM);
                this.nbgJof(this.MCaChp.AcPOPM);
            }
        } else {
            lJELmO.cJJPaG(this.JefDNA, this.MCaChp.AcPOPM);
        };
        this.HDNDed(false, false);
    };
    JpMdFf.prototype.inoPPG = function () {
        if (this.MCaChp) {
            if (this.MCaChp.MlomAd || this.MCaChp.parentNode) {
                this.HDNDed(true, false);
                this.MCaChp.MlomAd = null;
                this.MCaChp.NLedNa = false;
                this.MCaChp.classList.remove('deny');
                if (this.MCaChp.parentNode) {
                    this.MCaChp.parentNode.removeChild(this.MCaChp);
                }
            };
        }
    };
    JpMdFf.prototype.jjMaaf = function (ICPAOP, DNeceG, AcPOPM) {
        if (ICPAOP == 2) {
            ecoKAl.PMoLOf(this.DONAgB.DaBjli, AcPOPM);
            amlClm = this.DONAgB.eEmHpf[0];
            MEaoDC = this.DONAgB.eEmHpf[1];
            if (amlClm[0] == MEaoDC[0]) {
                if (AcPOPM[0] < amlClm[0]) {
                    AcPOPM[0] = amlClm[0];
                }
            } else {
                if (AcPOPM[1] < amlClm[1]) {
                    AcPOPM[1] = amlClm[1];
                }
            };
            var mMIEgh = lJELmO.NImECF(amlClm, AcPOPM);
            if (mMIEgh > this.DONAgB.eEmHpf[2]) {
                var jmAloE = lJELmO.khOMcp(AcPOPM, amlClm);
                lJELmO.dbagEB(jmAloE);
                lJELmO.dMdbkN(jmAloE, this.DONAgB.eEmHpf[2] - dDFAkd);
                jmAloE = lJELmO.mCMKjO(amlClm, jmAloE);
                lJELmO.BObpdE(jmAloE);
                lJELmO.cJJPaG(jmAloE, AcPOPM);
            }
        } else if (ICPAOP == 1) {
            ecoKAl.PMoLOf(this.DONAgB.gCipfF, AcPOPM);
        } else {
            ecoKAl.PMoLOf(this.DONAgB.DaBjli, AcPOPM);
        };
        var dLNKce = this.NmmCpf + JEpkfL;
        var fOGnCG, HNOFJb = this.pPGclC.length;
        for (fOGnCG = 0; fOGnCG < HNOFJb; fOGnCG++) {
            mhlkef = this.pPGclC[fOGnCG];
            if (mhlkef[0] != DNeceG) {
                if (mhlkef[1]) {
                    if (lJELmO.NImECF(AcPOPM, mhlkef[2]) < dLNKce) {
                        return false;
                    }
                };
            }
        };
        return true;
    };
    JpMdFf.prototype.KDJcda = function (MlomAd) {
        if (!MlomAd) {
            return;
        };
        this.eLHmnH = false;
        this.dCLkjM = MlomAd;
        this.dCLkjM.HolCMn = 0;
        window.setTimeout(this.pAinAi, 500, this);
    };
    JpMdFf.prototype.hIFbom = function () {
        if (!this.dCLkjM) {
            return;
        };
        this.AIIHhG.OgInlJ();
        this.eLHmnH = false;
        this.dCLkjM.HolCMn = 0;
        this.cFaPCi();
    };
    JpMdFf.prototype.oODIpi = function () {
        if (!this.dCLkjM) {
            return;
        };
        if (this.dCLkjM.HolCMn >= this.dCLkjM.MplMCo.length - 1) {
            return;
        };
        this.eLHmnH = true;
        this.AIIHhG.JJJgMI();
        this.AIIHhG.NBPlhb();
        this.AIIHhG.HjGcOh();
    };
    JpMdFf.prototype.jpAJGd = function () {
        if (!this.dCLkjM) {
            return;
        };
        this.eLHmnH = false;
        this.AIIHhG.afPMfG();
        if (!this.cnaFhk && !this.JENiKa) {
            this.cFaPCi();
        }
    };
    JpMdFf.prototype.pAinAi = function (EgNgBG) {
        if (!EgNgBG.dCLkjM || !EgNgBG.hBeflg) {
            return;
        };
        EgNgBG.cFaPCi();
    };
    JpMdFf.prototype.cFaPCi = function () {
        if (!this.hBeflg) {
            return;
        };
        var DILNMg, MBllBn, MlomAd, hoMDEC;
        var hCHoIl = false;
        if (this.CnokOK.length > 0) {
            MlomAd = this.CnokOK.shift();
            hoMDEC = MlomAd[0];
            if (hoMDEC != 'q') {
                this.iEJHDn(0);
                this.inoPPG();
            };
            if (hoMDEC == 'i') {
                this.ImnNgj = MlomAd[1];
                this.bBliJe(this.ImnNgj);
                this.AIIHhG.geEeHn();
                this.ojjAHN();
                hCHoIl = true;
            } else if (hoMDEC == 'z') {
                this.gIpBOH();
            } else if (hoMDEC == 's') {
                MlomAd.shift();
                this.hcBGoK(MlomAd);
            } else if (hoMDEC == 'a') {
                this.MDfoNP(NmbiKM(MlomAd[1]), NmbiKM(MlomAd[2]), NmbiKM(MlomAd[3]), false);
            } else if (hoMDEC == 'b') {
                this.fIPaLb(MlomAd);
            } else if (hoMDEC == 'c') {
                this.PlgLPp(MlomAd);
            } else if (hoMDEC == 'r') {
                this.MDfoNP(NmbiKM(MlomAd[1]), NmbiKM(MlomAd[2]), 0, true);
            } else if (hoMDEC == 'u') {
                DILNMg = NmbiKM(MlomAd[1]);
                var OPKHjd = this.kDBpDc(DILNMg);
                if (OPKHjd) {
                    var FcooBM = OPKHjd[6];
                    var CJHGCK = OPKHjd[7];
                    OPKHjd[1] = 1;
                    FcooBM.ifpaFO = [1, 1];
                    FcooBM.NhoOmg = 1;
                    CJHGCK.NhoOmg = 1;
                    OPKHjd[3][0] = 0;
                    OPKHjd[3][1] = 0;
                    OPKHjd[5] = 0;
                    if (OPKHjd[8]) {
                        OPKHjd[8].NhoOmg = 1;
                    };
                    OPKHjd[9] = 0;
                    OPKHjd[10] = 0;
                    OPKHjd[11] = null;
                    mhlkef[2][0] = mPIIDJ.llhDAb(MlomAd[3]);
                    mhlkef[2][1] = mPIIDJ.llhDAb(MlomAd[4]);
                    this.jMcjpd(mhlkef);
                    this.CipCaF.aGcIfL();
                };
                this.MDfoNP(DILNMg, NmbiKM(MlomAd[2]), 0, true);
            } else if (hoMDEC == 'q') {
                if (this.eAAjjm == 2) {
                    this.lLDEmb = HAELdp.HmHLIi(HAELdp.fNPoca(NmbiKM(MlomAd[1]) * 0.1));
                    this.BdimnP = true;
                }
            } else if (hoMDEC == 'p') {
                this.BePFKa(NmbiKM(MlomAd[1]), [NmbiKM(MlomAd[4]), NmbiKM(MlomAd[5])], [NmbiKM(MlomAd[6]), NmbiKM(MlomAd[7]), NmbiKM(MlomAd[8])], NmbiKM(MlomAd[2]), NmbiKM(MlomAd[3]), 2);
            } else if (hoMDEC == 'n') {
                DILNMg = null;
                if (MlomAd[3] != '') {
                    DILNMg = MlomAd[3].split(';');
                };
                MBllBn = null;
                if (MlomAd[4] != '') {
                    MBllBn = MlomAd[4].split(';');
                };
                this.HdnMpk(NmbiKM(MlomAd[1]), NmbiKM(MlomAd[2]), DILNMg, MBllBn);
            } else {
                $warn('GC ' + hoMDEC);
            }
        };
        if (this.BidDIf.length > 0 && !hCHoIl) {
            this.AIIHhG.OgInlJ();
            var pKaopF = this.BidDIf.shift();
            var LeNpNP = HAELdp.OHokFB(knJbka() - pKaopF[0]);
            MlomAd = pKaopF[1];
            var bmfhpd = MlomAd.length;
            for (var fOGnCG = 0; fOGnCG < bmfhpd; fOGnCG++) {
                DILNMg = MlomAd[fOGnCG].split('#');
                hoMDEC = DILNMg[0];
                if (hoMDEC == 'p') {
                    if (DILNMg.length < 4) {
                        this.AIIHhG.MHIJhF(DILNMg[1], GbiMej('computer_player'), DILNMg[3]);
                    } else {
                        this.AIIHhG.MHIJhF(DILNMg[1], DILNMg[2], DILNMg[3]);
                    }
                } else if (hoMDEC == 's') {
                    this.AIIHhG.JJCKFe(DILNMg[1], DILNMg[2]);
                } else if (hoMDEC == 'i') {
                    this.AIIHhG.odcMgf(DILNMg[1], DILNMg[2]);
                } else if (hoMDEC == 'h') {
                    this.AIIHhG.BlECiI(DILNMg[1], DILNMg[2]);
                } else if (hoMDEC == 'j') {
                    this.AIIHhG.emfbLG(DILNMg[1], DILNMg[2]);
                } else if (hoMDEC == 'c') {
                    this.AIIHhG.haNiCk(DILNMg[1]);
                } else if (hoMDEC == 't') {
                    this.AIIHhG.CdFBij(NmbiKM(DILNMg[1]) + LeNpNP, DILNMg[2]);
                } else if (hoMDEC == 'e') {
                    this.AIIHhG.jBilmk(DILNMg[1]);
                } else if (hoMDEC == 'r') {
                    this.AIIHhG.FJEcfm(DILNMg[1], NmbiKM(DILNMg[2]) + LeNpNP);
                } else if (hoMDEC == 'w') {
                    this.AIIHhG.HjGcOh();
                    this.iEJHDn(0);
                    this.inoPPG();
                    this.AIIHhG.aBNniF(DILNMg[1], DILNMg[2], DILNMg[3], DILNMg[4], DILNMg[5], DILNMg[6]);
                } else if (hoMDEC == 'b') {
                    if (DILNMg.length < 2) {
                        this.MOIged(null, false);
                    } else {
                        this.MOIged(DILNMg[1].split(';'), false);
                    }
                } else if (hoMDEC == 'k') {
                    this.KAGcGh(DILNMg[1].split(';'));
                } else if (hoMDEC == 'o') {
                    this.ojjAHN();
                } else if (hoMDEC == 'v') {
                    this.AIIHhG.gHDccP();
                    var FPNbFH = DILNMg.length;
                    for (var jGfFPE = 1; jGfFPE < FPNbFH; jGfFPE++) {
                        this.AIIHhG.MBnfai(DILNMg[jGfFPE]);
                    }
                } else if (hoMDEC == 'l') {
                    this.AIIHhG.MBnfai(DILNMg[1]);
                } else {
                    $warn('IC ' + hoMDEC);
                }
            };
        };
        if (this.CnokOK.length > 0 || this.BidDIf.length > 0) {
            this.cFaPCi();
        } else if (this.dCLkjM) {
            if (!this.cnaFhk && !this.JENiKa && !this.eLHmnH) {
                var HolCMn = this.dCLkjM.HolCMn;
                var MplMCo = this.dCLkjM.MplMCo;
                if (HolCMn < MplMCo.length) {
                    var fMnbiD = MplMCo[HolCMn];
                    HolCMn = HolCMn + 1;
                    this.dCLkjM.HolCMn = HolCMn;
                    this.jJNMeA(fMnbiD);
                } else {
                    this.AIIHhG.afPMfG();
                }
            };
        }
    };
    JpMdFf.prototype.jJNMeA = function (HLkCLj) {
        if (!this.hBeflg) {
            return;
        };
        if (!HLkCLj) {
            return;
        };
        if (HLkCLj.hasOwnProperty('gcn')) {
            this.AIIHhG.Ilmieb();
        };
        if (HLkCLj.hasOwnProperty('cpi')) {
            this.eAeFAO.LcJlao = NmbiKM(HLkCLj['cpi']);
        };
        var hKbcfc = false;
        if (HLkCLj.hasOwnProperty('gv')) {
            hKbcfc = true;
            var InIPKb = String(HLkCLj.gv).split('|');
            var bmfhpd = InIPKb.length;
            for (var fOGnCG = 0; fOGnCG < bmfhpd; fOGnCG++) {
                var AGbLFh = InIPKb[fOGnCG].split('#');
                var iMKLlL = AGbLFh[0];
                if (iMKLlL == 'z' || iMKLlL == 's') {
                    var deekEK = null;
                    var NhkbIl = this.CnokOK.length;
                    if (NhkbIl > 0) {
                        NhkbIl--;
                        if (this.CnokOK[NhkbIl][0] == 'i') {
                            deekEK = this.CnokOK[NhkbIl];
                        }
                    };
                    this.CnokOK = [AGbLFh];
                    if (deekEK) {
                        this.CnokOK.unshift(deekEK);
                    }
                } else {
                    this.CnokOK.push(AGbLFh);
                }
            };
        };
        if (HLkCLj.hasOwnProperty('gs')) {
            hKbcfc = true;
            this.BidDIf.push([knJbka(), String(HLkCLj.gs).split('|')]);
        };
        if (!this.cnaFhk && hKbcfc) {
            this.cFaPCi();
        }
    };
    JpMdFf.prototype.loNDBD = function (CGnGMk) {
        if (!this.hBeflg) {
            return;
        };
        if (this.GLJCMC > 0) {
            this.GLJCMC = 0;
        };
        if (this.cnaFhk) {
            this.ADEEjn();
        } else if (this.eAAjjm == 1) {
            this.maIOaI = lJELmO.hIoKBj(this.AFmPcM, this.oGjpOo);
            ggGkJc.nKCAoj(this.JgOAFb, this.maIOaI);
            this.JjahDc();
            if (this.gFednf) {
                this.dodcjj = this.dodcjj + (this.OhJEbo * BLAZE.paIPdi.KeOOoA);
                if (this.dodcjj > 1) {
                    this.dodcjj = 1;
                    this.OhJEbo = -this.OhJEbo;
                } else if (this.dodcjj <= 0) {
                    this.dodcjj = 0;
                    this.OhJEbo = -this.OhJEbo;
                };
                this.bKclpB();
            }
        } else if (this.eAAjjm == 2) {
            if (this.BdimnP) {
                EDdliE = this.lLDEmb;
                if (this.BkoHcI.hPEEGo) {
                    EDdliE = HAELdp.GGDAoj(EDdliE + HAELdp.eeNcng);
                };
                OdjMli = HAELdp.GGDAoj(EDdliE - this.IcjAkH);
                if (Math.abs(OdjMli) < IDGMhC) {
                    this.BdimnP = false;
                    this.IcjAkH = EDdliE;
                } else {
                    OdjMli = OdjMli * 0.1;
                    if (OdjMli > 0) {
                        if (OdjMli < IDGMhC) {
                            OdjMli = IDGMhC;
                        }
                    } else {
                        if (OdjMli > -IDGMhC) {
                            OdjMli = -IDGMhC;
                        }
                    };
                    this.IcjAkH = HAELdp.GGDAoj(this.IcjAkH + OdjMli);
                };
                ggGkJc.nKCAoj(this.JgOAFb, this.IcjAkH);
            }
        };
        if (BLAZE.bacjNj.lJbIhd(CGnGMk)) {
            if (!this.cnaFhk) {
                this.CipCaF.aGcIfL();
            }
        };
    };
    JpMdFf.prototype.oeLiEE = function () {
        if (this.lKGHhh && this.eAeFAO.oLnMib) {
            return true;
        };
        return false;
    };
    JpMdFf.prototype.IHFOKF = function () {
        if (!this.MKBPfJ) {
            return;
        };
        this.DKElck.style.display = 'none';
        this.FpMEcj.style.display = 'none';
        this.OcgFdh.style.display = 'none';
        this.MKBPfJ = false;
    };
    JpMdFf.prototype.NAekoa = function () {
        var bjJCfN = 0;
        if (this.oeLiEE()) {
            bjJCfN = 2;
            if (this.eAeFAO.hJJlNP) {
                bjJCfN = 3;
            }
        } else if (BLAZE.nhjLnH.lboAhk && this.eAeFAO.oLnMib) {
            bjJCfN = 1;
        };
        if (bjJCfN == 0) {
            if (this.MKBPfJ) {
                bjJCfN = 3;
                this.IHFOKF();
            };
            
        };
        amlClm = lJELmO.NoeNdn(this.FNNEFK);
        MEaoDC = lJELmO.NoeNdn(this.JefDNA);
        this.FMGaPH(MEaoDC);
        podbCd = lJELmO.khOMcp(MEaoDC, amlClm);
        EDdliE = HAELdp.BObpdE(lJELmO.PaaKha(podbCd) / dDFAkd * this.GJCkgG);
        lJELmO.dbagEB(podbCd);
        if (BLAZE.nhjLnH.lboAhk) {
            MEaoDC = lJELmO.PAGKnH(podbCd, 20000000);
            lJELmO.jeDgdF(MEaoDC, amlClm);
        };
        jGhjGb = [0];
        if (bjJCfN == 1) {
            oIieDj = true;
        } else {
            fBfhIC = lJELmO.NImECF(amlClm, MEaoDC);
            eLAKFi = this.bHBDje.length - 1;
            for (FdDBNA = 0; FdDBNA < eLAKFi; FdDBNA++) {
                HnPGCc = this.japcEB(amlClm, MEaoDC, this.bHBDje[FdDBNA], this.bHBDje[FdDBNA + 1]);
                if (HnPGCc) {
                    OdpkmM = lJELmO.NImECF(amlClm, HnPGCc);
                    if (OdpkmM < 0) {
                        OdpkmM = 0;
                    };
                    if (fBfhIC > OdpkmM) {
                        fBfhIC = OdpkmM;
                        jGhjGb[0] = 1;
                        jGhjGb[1] = this.bHBDje[FdDBNA];
                        jGhjGb[2] = this.bHBDje[FdDBNA + 1];
                        jGhjGb[3] = OdpkmM;
                        jGhjGb[4] = HnPGCc;
                        jGhjGb[5] = FdDBNA;
                    }
                };
            };
            if (bjJCfN == 3) {
                var OPKHjd = this.kDBpDc(this.oKpmDB);
                NOAbGk = OPKHjd[2];
                lKclNn = fBfhIC;
                fLoOmD = lJELmO.PAGKnH(podbCd, lKclNn);
                dgcnik = lJELmO.mCMKjO(NOAbGk, fLoOmD);
                bJefno = this.pPGclC;
                GIgPag = bJefno.length;
                for (OdjMli = 0; OdjMli < GIgPag; OdjMli++) {
                    Nhgpna = bJefno[OdjMli];
                    if (Nhgpna[1]) {
                        if (Nhgpna[0] != this.oKpmDB) {
                            KmkHIm = this.EgAJnM(fBfhIC, NOAbGk, dgcnik, fLoOmD, lKclNn, Nhgpna[2], Nhgpna[3]);
                            if (KmkHIm) {
                                fBfhIC = KmkHIm[0];
                                jGhjGb[0] = 2;
                                jGhjGb[1] = KmkHIm;
                                jGhjGb[2] = Nhgpna;
                            }
                        };
                    }
                };
            };
            oIieDj = true;
            if (jGhjGb[0] == 2) {
                KmkHIm = jGhjGb[1];
                MEaoDC = lJELmO.NoeNdn(KmkHIm[1]);
                podbCd = lJELmO.khOMcp(MEaoDC, amlClm);
                EDdliE = HAELdp.BObpdE(lJELmO.PaaKha(podbCd) / dDFAkd * this.GJCkgG);
                lJELmO.dbagEB(podbCd);
                lJELmO.dMdbkN(podbCd, dDFAkd);
                oIieDj = false;
                EPJHkf = this.DKElck.style;
                EPJHkf.display = '';
                this.DhcNbm(amlClm);
                lJELmO.IFDeod(amlClm, this.LoELbN);
                lJELmO.BObpdE(amlClm);
                EPJHkf.left = amlClm[0] + 'px';
                EPJHkf.top = amlClm[1] + 'px';
                this.PbbfcC.style.width = EDdliE + 'px';
                ggGkJc.nKCAoj(this.DKElck, lJELmO.IHmieI(podbCd));
                EPJHkf = this.FpMEcj.style;
                EPJHkf.display = '';
                this.DhcNbm(MEaoDC);
                lJELmO.IFDeod(MEaoDC, this.LoELbN);
                lJELmO.BObpdE(MEaoDC);
                EPJHkf.left = MEaoDC[0] + 'px';
                EPJHkf.top = MEaoDC[1] + 'px';
                ipgmHM = KmkHIm[2];
                EObkea = HAELdp.BObpdE(lJELmO.PaaKha(ipgmHM));
                this.KLGIdh.style.width = HAELdp.BObpdE((EObkea / lKclNn * 300) * this.GJCkgG)+800 + 'px';
                ggGkJc.nKCAoj(this.FpMEcj, lJELmO.IHmieI(ipgmHM));
                EPJHkf = this.OcgFdh.style;
                EPJHkf.display = '';
                Nhgpna = jGhjGb[2];
                MEaoDC = lJELmO.NoeNdn(Nhgpna[2]);
                this.DhcNbm(MEaoDC);
                lJELmO.IFDeod(MEaoDC, this.LoELbN);
                lJELmO.BObpdE(MEaoDC);
                EPJHkf.left = MEaoDC[0] + 'px';
                EPJHkf.top = MEaoDC[1] + 'px';
                ipgmHM = KmkHIm[3];
                EObkea = HAELdp.BObpdE(lJELmO.PaaKha(ipgmHM));
                this.GLcnGe.style.width = HAELdp.BObpdE((EObkea / lKclNn * 300) * this.GJCkgG) + 1000 + 'px';
                ggGkJc.nKCAoj(this.OcgFdh, lJELmO.IHmieI(ipgmHM));
            } else if (jGhjGb[0] > 0) {
                this.OcgFdh.style.display = 'none';
                MEaoDC = jGhjGb[4];
                if (jGhjGb[1][2] == 0 || jGhjGb[1][2] == null) {
                    podbCd = lJELmO.khOMcp(MEaoDC, amlClm);
                    EDdliE = HAELdp.BObpdE(lJELmO.PaaKha(podbCd) / dDFAkd * this.GJCkgG);
                    lJELmO.dbagEB(podbCd);
                    lJELmO.dMdbkN(podbCd, dDFAkd);
                    ipgmHM = this.iaGfJl(podbCd, jGhjGb[1], jGhjGb[2]);
                    IedkAJ = lJELmO.PAGKnH(ipgmHM, GdeJPB[0] * 2);
                    lJELmO.jeDgdF(IedkAJ, MEaoDC);
                    EPJHkf = jGhjGb[5];
                    fBfhIC = 99999999;
                    AapNgp = null;
                    for (FdDBNA = 0; FdDBNA < eLAKFi; FdDBNA++) {
                        if (FdDBNA != EPJHkf) {
                            HnPGCc = this.japcEB(MEaoDC, IedkAJ, this.bHBDje[FdDBNA], this.bHBDje[FdDBNA + 1]);
                            if (HnPGCc) {
                                OdpkmM = lJELmO.NImECF(MEaoDC, HnPGCc);
                                if (OdpkmM < 0) {
                                    OdpkmM = 0;
                                };
                                if (fBfhIC > OdpkmM) {
                                    fBfhIC = OdpkmM;
                                    AapNgp = HnPGCc;
                                }
                            };
                        }
                    };
                    if (AapNgp) {
                        oIieDj = false;
                        EPJHkf = this.DKElck.style;
                        EPJHkf.display = '';
                        this.DhcNbm(amlClm);
                        lJELmO.IFDeod(amlClm, this.LoELbN);
                        lJELmO.BObpdE(amlClm);
                        EPJHkf.left = amlClm[0] + 'px';
                        EPJHkf.top = amlClm[1] + 'px';
                        this.PbbfcC.style.width = EDdliE + 'px';
                        ggGkJc.nKCAoj(this.DKElck, lJELmO.IHmieI(podbCd));
                        EPJHkf = this.FpMEcj.style;
                        EPJHkf.display = '';
                        this.DhcNbm(MEaoDC);
                        lJELmO.IFDeod(MEaoDC, this.LoELbN);
                        lJELmO.BObpdE(MEaoDC);
                        EPJHkf.left = MEaoDC[0] + 'px';
                        EPJHkf.top = MEaoDC[1] + 'px';
                        this.KLGIdh.style.width = HAELdp.BObpdE(fBfhIC / dDFAkd * this.GJCkgG) + 'px';
                        ggGkJc.nKCAoj(this.FpMEcj, lJELmO.IHmieI(ipgmHM));
                    }
                };
            }
        };
        if (oIieDj) {
            this.FpMEcj.style.display = 'none';
            this.OcgFdh.style.display = 'none';
            lJELmO.dMdbkN(podbCd, dDFAkd);
            EPJHkf = this.DKElck.style;
            EPJHkf.display = '';
            this.DhcNbm(amlClm);
            lJELmO.IFDeod(amlClm, this.LoELbN);
            lJELmO.BObpdE(amlClm);
            EPJHkf.left = amlClm[0] + 'px';
            EPJHkf.top = amlClm[1] + 'px';
            this.PbbfcC.style.width = EDdliE + 'px';
            ggGkJc.nKCAoj(this.DKElck, lJELmO.IHmieI(podbCd));
        };
        this.MKBPfJ = true;
    };
    JpMdFf.prototype.MDfoNP = function (oKcffn, jJEIOG, nILmCh, IMjkOH) {
        if (!this.hBeflg) {
            return;
        };
        if (!this.JgOAFb) {
            return;
        };
        if (!this.JgOAFb.parentNode) {
            this.OlGPmN.appendChild(this.JgOAFb);
        };
        if (nILmCh >= 0) {
            BLAZE.bacjNj.HhbJel(nILmCh);
        };
        this.GndaMA = 0;
        this.GFcFhe = -1;
        this.JENiKa = false;
        this.cnaFhk = false;
        this.gFednf = false;
        oKcffn = NmbiKM(oKcffn);
        mhlkef = this.kDBpDc(oKcffn);
        if (!mhlkef) {
            return;
        };
        if (!mhlkef[1]) {
            return;
        };
        this.oKpmDB = oKcffn;
        this.iNbfnE.style.top = HAELdp.BObpdE(this.GJCkgG * hhGIpP) + 'px';
        this.dodcjj = 0;
        this.OhJEbo = afLliH;
        this.FNNEFK = lJELmO.NoeNdn(mhlkef[2]);
        lJELmO.cJJPaG(this.FNNEFK, this.AFmPcM);
        this.nbgJof(this.AFmPcM, this.OlGPmN);
        lJELmO.IFDeod(this.AFmPcM, this.KcMlaa);
        this.JgOAFb.style.left = this.AFmPcM[0] + 'px';
        this.JgOAFb.style.top = this.AFmPcM[1] + 'px';
        if (IMjkOH) {
            this.eAAjjm = 2;
        } else {
            this.eAAjjm = 1;
            this.GndaMA = knJbka();
            this.bNplck();
            this.OfLebf();
            this.aEFJcb();
            this.NAekoa();
        };
        this.IcjAkH = lJELmO.hIoKBj(this.AFmPcM, this.oGjpOo);
        ggGkJc.nKCAoj(this.JgOAFb, this.IcjAkH);
        jJEIOG = NmbiKM(jJEIOG);
        if (jJEIOG >= 0) {
            var NnOjHN = '';
            var bKbfjo, plbgkl;
            if (jJEIOG < 100) {
                bKbfjo = 'cue' + jJEIOG;
            } else if (jJEIOG < 1000) {
                jJEIOG -= 100;
                bKbfjo = 'pcue' + (jJEIOG);
            } else {
                jJEIOG -= 1000;
                bKbfjo = 'acue' + (jJEIOG);
            };
            if (this.lPColI == bKbfjo) {
                if (bKbfjo.substring(0, 4) == 'acue') {
                    this.EJeBcH.classList.add('sprite');
                    plbgkl = BjmnkM[jJEIOG];
                    this.JNGiGP.style.top = plbgkl[0] + '%';
                    this.JNGiGP.style.bottom = (100 - plbgkl[0] - 50) + '%';
                    hkdcJB.ogbElm(this.JNGiGP, plbgkl[3], plbgkl[1], plbgkl[2]);
                }
            } else {
                var LOJjiI = false;
                if (jJEIOG == 0) {
                    NnOjHN = this.gAhNem.standard;
                } else {
                    this.lPColI = '';
                    if (this.gAhNem[bKbfjo]) {
                        NnOjHN = this.gAhNem[bKbfjo];
                    } else {
                        BLAZE.nhjLnH.dkgJMA(bKbfjo, PMFAbI + bKbfjo + '.png?' + BLAZE.CONTENT_VERSION, 1, this.oackNC, this);
                        if (this.gAhNem[bKbfjo]) {
                            NnOjHN = this.gAhNem[bKbfjo];
                        } else {
                            NnOjHN = this.gAhNem.standard;
                            LOJjiI = true;
                        }
                    };
                };
                this.lPColI = bKbfjo;
                this.EJeBcH.style.backgroundImage = NnOjHN;
                if (bKbfjo.substring(0, 4) == 'acue' && !LOJjiI) {
                    this.EJeBcH.classList.add('sprite');
                    this.JNGiGP.style.backgroundImage = NnOjHN;
                    plbgkl = BjmnkM[jJEIOG];
                    this.JNGiGP.style.top = plbgkl[0] + '%';
                    this.JNGiGP.style.bottom = (100 - plbgkl[0] - 50) + '%';
                    hkdcJB.ogbElm(this.JNGiGP, plbgkl[3], plbgkl[1], plbgkl[2]);
                } else {
                    this.EJeBcH.classList.remove('sprite');
                    this.JNGiGP.style.backgroundImage = '';
                    hkdcJB.EopacH(this.JNGiGP, true);
                }
            };
        }
    };
    JpMdFf.prototype.iEJHDn = function (jHCEiD) {
        if (!this.hBeflg) {
            return;
        };
        this.lkBoBC();
        this.FAmGFK();
        this.IHFOKF();
        this.eAAjjm = 0;
        this.GndaMA = 0;
        this.GFcFhe = -1;
        this.gFednf = false;
        if (!this.JgOAFb) {
            return;
        };
        if (this.JgOAFb.parentNode) {
            jHCEiD = NmbiKM(jHCEiD);
            if (jHCEiD > 0) {
                window.setTimeout(this.nfiOFO, jHCEiD, this);
            } else {
                hkdcJB.EopacH(this.JNGiGP, true);
                this.JgOAFb.parentNode.removeChild(this.JgOAFb);
            }
        };
    };
    JpMdFf.prototype.nfiOFO = function (EgNgBG) {
        if (EgNgBG) {
            if (EgNgBG.JgOAFb.parentNode && EgNgBG.eAAjjm == 0) {
                hkdcJB.EopacH(EgNgBG.JNGiGP, true);
                EgNgBG.JgOAFb.parentNode.removeChild(EgNgBG.JgOAFb);
            }
        };
    };
    JpMdFf.prototype.JjahDc = function (EpDhoe) {
        if (this.eAAjjm != 1 || !this.eAeFAO.jHIGoB) {
            return;
        };
        var DILNMg = HAELdp.BObpdE(HAELdp.fNPoca(HAELdp.oAEidp(this.maIOaI)) * 10);
        if (Math.abs(this.GFcFhe - DILNMg) < 20) {
            return;
        };
        var gLlGJe = BLAZE.paIPdi.gniGfc;
        if (gLlGJe - this.GndaMA > HFOgdh) {
            this.GndaMA = gLlGJe;
            this.GFcFhe = DILNMg;
            this.AIIHhG.DJMNpK({
                c: 'q',
                v: DILNMg
            });
        }
    };
    JpMdFf.prototype.bKclpB = function () {
        if (!this.JgOAFb) {
            return;
        };
        this.iNbfnE.style.top = HAELdp.BObpdE(this.GJCkgG * (hhGIpP + (this.dodcjj * EiDDdo))) + 'px';
    };
    JpMdFf.prototype.aEFJcb = function () {
        lJELmO.cJJPaG(this.JefDNA, this.oGjpOo);
        lJELmO.IFDeod(this.oGjpOo, this.KcMlaa);
        lJELmO.BObpdE(this.oGjpOo);
    };
    JpMdFf.prototype.bNplck = function () {
        if (this.KEMAdJ[0] != 0 || this.KEMAdJ[1] != 0 || this.CGLcbM != 0) {
            this.KEMAdJ[0] = 0;
            this.KEMAdJ[1] = 0;
            this.CGLcbM = 0;
            if (this.gdceHj) {
                var MBllBn = this.gdceHj.FeKiLh.point.style;
                MBllBn.left = '90px';
                MBllBn.top = '90px';
                ggGkJc.nKCAoj(this.gdceHj.FeKiLh.angle, 0);
            }
        };
    };
    JpMdFf.prototype.cgiHPO = function () {
        if (this.gdceHj) {
            if (this.gdceHj.parentNode) {
                return true;
            }
        };
        return false;
    };
    JpMdFf.prototype.IkINaD = function () {
        if (!this.ebkjkE) {
            return;
        };
        this.pKfEKp = false;
        if (!this.gdceHj || this.eAAjjm != 1) {
            return;
        };
        if (!this.gdceHj.parentNode) {
            this.OlGPmN.appendChild(this.gdceHj);
        };
        this.laLjpB();
    };
    JpMdFf.prototype.FAmGFK = function () {
        this.pKfEKp = false;
        if (this.gdceHj) {
            if (this.gdceHj.parentNode) {
                this.gdceHj.parentNode.removeChild(this.gdceHj);
            }
        };
    };
    JpMdFf.prototype.laLjpB = function () {
        if (!this.gdceHj) {
            return;
        };
        if (!this.gdceHj.parentNode) {
            return;
        };
        var gPDLaF = ggGkJc.KkjAMO();
        gPDLaF[2] -= 90;
        gPDLaF[3] -= 90;
        var ahFpKA = lJELmO.NoeNdn(this.FNNEFK);
        this.nbgJof(ahFpKA);
        lJELmO.IFDeod(ahFpKA, this.KcMlaa);
        if (ahFpKA[0] < 90) {
            ahFpKA[0] = 90;
        } else if (ahFpKA[0] > gPDLaF[2]) {
            ahFpKA[0] = gPDLaF[2];
        };
        if (ahFpKA[1] < 90) {
            ahFpKA[1] = 90;
        } else if (ahFpKA[1] > gPDLaF[3]) {
            ahFpKA[1] = gPDLaF[3];
        };
        lJELmO.BObpdE(ahFpKA);
        this.gdceHj.style.left = ahFpKA[0] + 'px';
        this.gdceHj.style.top = ahFpKA[1] + 'px';
        lJELmO.jeDgdF(ahFpKA, this.KcMlaa);
        this.gdceHj.dMBdhi = ahFpKA;
    };
    JpMdFf.prototype.PGNgCB = function (AcPOPM) {
        if (!this.gdceHj) {
            return;
        };
        if (!this.gdceHj.parentNode) {
            return;
        };
        var MBllBn, feEgiC = this.gdceHj.dMBdhi;
        var GnIbgg = lJELmO.NImECF(feEgiC, AcPOPM);
        if (GnIbgg <= 50) {
            var HNFfMb = 30;
            if (GnIbgg > HNFfMb) {
                GnIbgg = HNFfMb;
            };
            lJELmO.IFDeod(AcPOPM, feEgiC);
            var fKhDmM = lJELmO.NoeNdn(AcPOPM);
            lJELmO.dbagEB(fKhDmM);
            lJELmO.dMdbkN(fKhDmM, GnIbgg);
            lJELmO.cJJPaG(fKhDmM, AcPOPM);
            lJELmO.HpDGlG(fKhDmM, HNFfMb);
            if (fKhDmM[0] < -1) {
                fKhDmM[0] = -1;
            } else if (fKhDmM[0] > 1) {
                fKhDmM[0] = 1;
            };
            if (fKhDmM[1] < -1) {
                fKhDmM[1] = -1;
            } else if (fKhDmM[1] > 1) {
                fKhDmM[1] = 1;
            };
            lJELmO.cJJPaG(fKhDmM, this.KEMAdJ);
            lJELmO.jeDgdF(AcPOPM, [90, 90]);
            lJELmO.BObpdE(AcPOPM);
            MBllBn = this.gdceHj.FeKiLh.point.style;
            MBllBn.left = AcPOPM[0] + 'px';
            MBllBn.top = AcPOPM[1] + 'px';
        } else {
            var knCDGC = 0.94;
            var JMbfLA = HAELdp.eeNcng - lJELmO.hIoKBj(feEgiC, AcPOPM);
            if (JMbfLA <= (knCDGC + 0.03) && JMbfLA >= -0.03) {
                if (JMbfLA > knCDGC) {
                    JMbfLA = knCDGC;
                } else if (JMbfLA < 0) {
                    JMbfLA = 0;
                };
                this.CGLcbM = JMbfLA / knCDGC;
                ggGkJc.nKCAoj(this.gdceHj.FeKiLh.angle, -JMbfLA);
            }
        };
    };
    JpMdFf.prototype.lkBoBC = function () {
        if (this.GeBcJp) {
            this.GeBcJp.classList.remove('active');
            if (this.GeBcJp.parentNode) {
                this.GeBcJp.parentNode.removeChild(this.GeBcJp);
            }
        };
    };
    JpMdFf.prototype.OfLebf = function () {
        if (!this.ebkjkE) {
            return;
        };
        if (!this.GeBcJp) {
            this.GeBcJp = BLAZE.nhjLnH.oAclpm('element', 'game.billiards_spin_button');
            this.GeBcJp.classList.remove('active');
        };
        if (!this.GeBcJp.parentNode) {
            this.LcdpGp.FeKiLh.table_markers.appendChild(this.GeBcJp);
        };
        var PDipmG = Math.round(this.NmmCpf / dDFAkd * this.GJCkgG + nHpnEC);
        var ndijOA = Math.round(PDipmG * -0.5);
        var MBllBn = this.GeBcJp.style;
        PDipmG = PDipmG + 'px';
        MBllBn.margin = ndijOA + 'px 0 0 ' + ndijOA + 'px';
        MBllBn.width = PDipmG;
        MBllBn.height = PDipmG;
        this.HJgeKM();
        this.GeBcJp.classList.add('active');
    };
    JpMdFf.prototype.HJgeKM = function () {
        if (!this.ebkjkE) {
            return;
        };
        if (!this.GeBcJp) {
            return;
        };
        if (!this.GeBcJp.parentNode) {
            return;
        };
        var nmKbDC = ggGkJc.oAcDfp(this.GeBcJp.parentNode);
        var leDCbg = lJELmO.NoeNdn(this.FNNEFK);
        this.DhcNbm(leDCbg);
        lJELmO.IFDeod(leDCbg, nmKbDC);
        lJELmO.BObpdE(leDCbg);
        var MBllBn = this.GeBcJp.style;
        MBllBn.left = leDCbg[0] + 'px';
        MBllBn.top = leDCbg[1] + 'px';
    };
    JpMdFf.prototype.DJafbE = function () {
        if (!this.fghCeo) {
            return;
        };
        this.FAmGFK();
        var bmfhpd = this.dPOkmj.length;
        for (var fOGnCG = 0; fOGnCG < bmfhpd; fOGnCG++) {
            var fMnbiD = this.dPOkmj[fOGnCG];
            if (fMnbiD.parentNode) {
                fMnbiD.parentNode.removeChild(fMnbiD);
            }
        };
        this.nDIkHO = false;
        this.fghCeo = null;
    };
    JpMdFf.prototype.ojjAHN = function () {
        if (!this.FFaNCh) {
            return;
        };
        var bmfhpd = this.DgGcoe.length;
        for (var fOGnCG = 0; fOGnCG < bmfhpd; fOGnCG++) {
            var fMnbiD = this.DgGcoe[fOGnCG];
            if (fMnbiD.parentNode) {
                fMnbiD.parentNode.removeChild(fMnbiD);
            }
        };
        this.FFaNCh = null;
    };
    JpMdFf.prototype.MOIged = function (LJhpGD, ICOoHa) {
        this.DJafbE();
        var fOGnCG, HIhniL, HNOFJb;
        if (!LJhpGD) {
            LJhpGD = [];
            HNOFJb = this.pPGclC.length;
            for (fOGnCG = 0; fOGnCG < HNOFJb; fOGnCG++) {
                LJhpGD.push(this.pPGclC[fOGnCG][0]);
            }
        };
        this.fghCeo = LJhpGD;
        this.nDIkHO = ICOoHa;
        var dPAfkA = this.LcdpGp.FeKiLh.table_markers;
        var nmKbDC = ggGkJc.oAcDfp(dPAfkA);
        var PDipmG = Math.round(this.NmmCpf / dDFAkd * this.GJCkgG + nHpnEC);
        var ndijOA = Math.round(PDipmG * -0.5);
        ndijOA = ndijOA + 'px 0 0 ' + ndijOA + 'px';
        PDipmG = PDipmG + 'px';
        var EKjeoM = 'BilliardsBallMarker';
        if (ICOoHa) {
            EKjeoM = 'BilliardsBallMarkerSelect';
        };
        HNOFJb = LJhpGD.length;
        for (fOGnCG = this.dPOkmj.length; fOGnCG < HNOFJb; fOGnCG++) {
            this.dPOkmj.push(document.createElement('div'));
        };
        for (fOGnCG = 0; fOGnCG < HNOFJb; fOGnCG++) {
            var OPKHjd = this.kDBpDc(NmbiKM(LJhpGD[fOGnCG]));
            if (OPKHjd) {
                if (OPKHjd[1]) {
                    var leDCbg = lJELmO.NoeNdn(OPKHjd[2]);
                    this.DhcNbm(leDCbg);
                    lJELmO.IFDeod(leDCbg, nmKbDC);
                    lJELmO.BObpdE(leDCbg);
                    var fMnbiD = this.dPOkmj[fOGnCG];
                    var MBllBn = fMnbiD.style;
                    fMnbiD.className = EKjeoM;
                    MBllBn.left = leDCbg[0] + 'px';
                    MBllBn.top = leDCbg[1] + 'px';
                    MBllBn.width = PDipmG;
                    MBllBn.height = PDipmG;
                    MBllBn.margin = ndijOA;
                    dPAfkA.appendChild(fMnbiD);
                    if (ICOoHa) {
                        hOFFNd.foifJe(fMnbiD, this.ihklbm, [this, OPKHjd[0]], false);
                    }
                };
            }
        };
    };
    JpMdFf.prototype.KAGcGh = function (LJhpGD) {
        this.ojjAHN();
        this.FFaNCh = LJhpGD;
        var dPAfkA = this.LcdpGp.FeKiLh.table_markers;
        var nmKbDC = ggGkJc.oAcDfp(dPAfkA);
        var PDipmG = Math.round(JMeCBB * this.GJCkgG);
        var BlpGKj = Math.round(NHocha * this.GJCkgG);
        if (BlpGKj < 1) {
            BlpGKj = 1;
        };
        var ndijOA = Math.round(PDipmG * -0.5);
        ndijOA = ndijOA + 'px 0 0 ' + ndijOA + 'px';
        PDipmG = PDipmG + 'px';
        var EKjeoM = 'BilliardsPocketMarker marker_';
        var fOGnCG, HIhniL, DILNMg, HNOFJb = LJhpGD.length;
        for (fOGnCG = this.DgGcoe.length; fOGnCG < HNOFJb; fOGnCG++) {
            this.DgGcoe.push(document.createElement('div'));
        };
        for (fOGnCG = 0; fOGnCG < HNOFJb; fOGnCG++) {
            HIhniL = LJhpGD[fOGnCG].split(':');
            if (HIhniL.length == 2) {
                var AKJHGD = this.ebDANl['_' + HIhniL[0]];
                if (AKJHGD) {
                    AKJHGD = lJELmO.NoeNdn(AKJHGD);
                    this.DhcNbm(AKJHGD);
                    lJELmO.IFDeod(AKJHGD, nmKbDC);
                    lJELmO.BObpdE(AKJHGD);
                    var fMnbiD = this.DgGcoe[fOGnCG];
                    var MBllBn = fMnbiD.style;
                    fMnbiD.className = EKjeoM + HIhniL[1];
                    MBllBn.left = AKJHGD[0] + 'px';
                    MBllBn.top = AKJHGD[1] + 'px';
                    MBllBn.width = PDipmG;
                    MBllBn.height = PDipmG;
                    MBllBn.margin = ndijOA;
                    MBllBn.borderWidth = BlpGKj + 'px';
                    dPAfkA.appendChild(fMnbiD);
                }
            };
        }
    };
    JpMdFf.prototype.ihklbm = function (EgNgBG, oKcffn) {
        oKcffn = NmbiKM(oKcffn);
        if (oKcffn < 0) {
            return;
        };
        if (EgNgBG.eAeFAO.jHIGoB) {
            EgNgBG.AIIHhG.DJMNpK({
                c: 'chs',
                v: oKcffn
            });
        };
        EgNgBG.MDfoNP(oKcffn, NmbiKM(EgNgBG.mEpLnC[1]), NmbiKM(EgNgBG.mEpLnC[2]), false);
        EgNgBG.mEpLnC = null;
        EgNgBG.DJafbE();
    };
    JpMdFf.prototype.PlgLPp = function (MlomAd) {
        this.mEpLnC = MlomAd;
        this.MOIged(null, true);
    };
    JpMdFf.prototype.FaPmCf = function () {
        if (this.eAAjjm != 1) {
            return;
        };
        mhlkef = this.kDBpDc(this.oKpmDB);
        if (!mhlkef) {
            return;
        };
        if (!mhlkef[1]) {
            return;
        };
        var AcPOPM = lJELmO.NoeNdn(this.JefDNA);
        this.FMGaPH(AcPOPM);
        if (lJELmO.NImECF(AcPOPM, mhlkef[2]) < this.NmmCpf) {
            this.IkINaD();
            return;
        };
        this.gFednf = true;
    };
    JpMdFf.prototype.PbdFPp = function (AcPOPM) {
        if (!this.gFednf || this.eAAjjm != 1) {
            return;
        };
        this.gFednf = false;
        mhlkef = this.kDBpDc(this.oKpmDB);
        if (!mhlkef) {
            return;
        };
        if (!mhlkef[1]) {
            return;
        };
        var AcPOPM = lJELmO.NoeNdn(this.JefDNA);
        var DhebFO = this.dodcjj;
        if (DhebFO > 0.7) {
            DhebFO = DhebFO * 1.15;
        } else if (DhebFO < 0.3) {
            DhebFO = DhebFO * 0.9;
        };
        if (DhebFO < ooFOBc) {
            DhebFO = ooFOBc;
        } else if (DhebFO > 1) {
            DhebFO = 1;
        };
        this.FMGaPH(AcPOPM);
        lJELmO.IFDeod(AcPOPM, mhlkef[2]);
        lJELmO.dbagEB(AcPOPM);
        lJELmO.dMdbkN(AcPOPM, this.pnkKjh * DhebFO);
        var ccgPCC;
        if (this.ebkjkE) {
            ccgPCC = lJELmO.NoeNdn(this.KEMAdJ);
            ccgPCC[2] = this.CGLcbM;
            ccgPCC[0] = HAELdp.BObpdE(ccgPCC[0] * 1000);
            ccgPCC[1] = HAELdp.BObpdE(ccgPCC[1] * 1000);
            ccgPCC[2] = HAELdp.BObpdE(ccgPCC[2] * 1000);
        } else {
            ccgPCC = [0, 0, 0];
        };
        this.BePFKa(this.oKpmDB, AcPOPM, ccgPCC, -1, -1, 0);
    };
    JpMdFf.prototype.DHpnNm = function (EAmjJJ) {
        if (this.dCLkjM) {
            this.oODIpi();
        } else {
            if (this.cgiHPO()) {
                this.FAmGFK();
                return;
            };
            this.JefDNA[0] = EAmjJJ.clientX;
            this.JefDNA[1] = EAmjJJ.clientY;
            if (this.eAAjjm == 1) {
                EAmjJJ.preventDefault();
                EAmjJJ.stopPropagation();
                this.aEFJcb();
                this.FaPmCf();
                this.NAekoa();
            }
        };
    };
    JpMdFf.prototype.AHgKJg = function (EAmjJJ) {
        if (EAmjJJ.target) {
            if (EAmjJJ.target.id.substr(0, 12) == 'videoplayer_' || EAmjJJ.target.id.substr(0, 16) == 'instagramplayer_') {
                return;
            }
        };
        if (this.cgiHPO()) {
            EAmjJJ.preventDefault();
            EAmjJJ.stopPropagation();
            this.pKfEKp = false;
            return;
        };
        this.JefDNA[0] = EAmjJJ.clientX;
        this.JefDNA[1] = EAmjJJ.clientY;
        if (this.eAAjjm == 1) {
            if (EAmjJJ.target) {
                EAmjJJ.preventDefault();
                EAmjJJ.stopPropagation();
                this.aEFJcb();
                this.PbdFPp();
            }
        } else if (this.MCaChp.MlomAd) {
            if (EAmjJJ.target) {
                if (EAmjJJ.target.KJkiNL || EAmjJJ.target.FmfGpK) {
                    this.fHepCk();
                }
            };
        }
    };
    JpMdFf.prototype.khPphk = function (EAmjJJ) {
        if (this.cgiHPO()) {
            if (this.pKfEKp) {
                this.PGNgCB([EAmjJJ.clientX, EAmjJJ.clientY]);
            };
            return;
        };
        this.JefDNA[0] = EAmjJJ.clientX;
        this.JefDNA[1] = EAmjJJ.clientY;
        if (this.eAAjjm == 1) {
            this.aEFJcb();
            this.NAekoa();
        } else if (this.MCaChp.MlomAd) {
            lJELmO.cJJPaG(this.JefDNA, this.MCaChp.AcPOPM);
            this.HDNDed(false, false);
        }
    };
    JpMdFf.prototype.pacHco = function (EAmjJJ) {
        if (EAmjJJ.changedTouches.length < 1) {
            return;
        };
        var lboAhk = EAmjJJ.changedTouches[0];
        if (lboAhk.target) {
            if (lboAhk.target.id == 'RoomChatInput') {
                return;
            }
        };
        if (this.dCLkjM) {
            EAmjJJ.preventDefault();
            EAmjJJ.stopPropagation();
            this.oODIpi();
        } else {
            if (this.cgiHPO()) {
                this.FAmGFK();
                return;
            };
            this.JefDNA[0] = lboAhk.clientX;
            this.JefDNA[1] = lboAhk.clientY;
            if (this.eAAjjm == 1) {
                this.aEFJcb();
                this.FaPmCf();
                this.NAekoa();
            } else if (this.MCaChp.MlomAd) {
                if (EAmjJJ.target) {
                    if (EAmjJJ.target.KJkiNL || EAmjJJ.target.FmfGpK) {
                        this.BcLMBg();
                    }
                };
            }
        };
    };
    JpMdFf.prototype.cHBChG = function (EAmjJJ) {
        if (this.cgiHPO()) {
            EAmjJJ.preventDefault();
            EAmjJJ.stopPropagation();
            this.pKfEKp = false;
            return;
        };
        if (EAmjJJ.changedTouches.length < 1) {
            return;
        };
        var lboAhk = EAmjJJ.changedTouches[0];
        if (lboAhk.target) {
            if (lboAhk.target.id == 'RoomChatInput') {
                return;
            }
        };
        this.JefDNA[0] = lboAhk.clientX;
        this.JefDNA[1] = lboAhk.clientY;
        if (this.MCaChp.MlomAd) {
            if (EAmjJJ.target) {
                if (EAmjJJ.target.KJkiNL || EAmjJJ.target.FmfGpK) {
                    this.fHepCk();
                    EAmjJJ.preventDefault();
                    EAmjJJ.stopPropagation();
                }
            };
        } else if (this.eAAjjm == 1) {
            EAmjJJ.preventDefault();
            EAmjJJ.stopPropagation();
            this.aEFJcb();
            this.PbdFPp();
        }
    };
    JpMdFf.prototype.LDLgJP = function (EAmjJJ) {
        if (this.cgiHPO()) {
            this.pKfEKp = false;
        };
        if (this.eAAjjm == 1) {
            this.gFednf = false;
        }
    };
    JpMdFf.prototype.lkkAbJ = function (EAmjJJ) {
        if (EAmjJJ.changedTouches.length < 1) {
            return;
        };
        var lboAhk = EAmjJJ.changedTouches[0];
        if (this.cgiHPO()) {
            if (this.pKfEKp) {
                this.PGNgCB([lboAhk.clientX, lboAhk.clientY]);
            };
            return;
        };
        this.JefDNA[0] = lboAhk.clientX;
        this.JefDNA[1] = lboAhk.clientY;
        if (this.eAAjjm == 1) {
            this.aEFJcb();
            this.NAekoa();
        } else if (this.MCaChp.MlomAd) {
            lJELmO.cJJPaG(this.JefDNA, this.MCaChp.AcPOPM);
            this.HDNDed(false, false);
        }
    };
    JpMdFf.prototype.CllplA = function (EAmjJJ) {
        EAmjJJ.preventDefault();
        EAmjJJ.stopPropagation();
    };
    JpMdFf.prototype.FLJegn = function () {
        if (!BLAZE.nhjLnH.lboAhk) {
            this.FAmGFK();
        }
    };
    JpMdFf.prototype.GmAfbE = function (EAmjJJ) {
        if (this.cgiHPO()) {
            EAmjJJ.preventDefault();
            EAmjJJ.stopPropagation();
            this.pKfEKp = true;
            this.PGNgCB([EAmjJJ.clientX, EAmjJJ.clientY]);
            return;
        }
    };
    JpMdFf.prototype.cdfANN = function (EAmjJJ) {
        if (EAmjJJ.changedTouches.length < 1) {
            return;
        };
        var lboAhk = EAmjJJ.changedTouches[0];
        if (this.cgiHPO()) {
            EAmjJJ.preventDefault();
            EAmjJJ.stopPropagation();
            this.pKfEKp = true;
            this.PGNgCB([lboAhk.clientX, lboAhk.clientY]);
            return;
        }
    };
    JpMdFf.prototype.iIKgJL = function (EdpPKD, GmbBoJ, fabDgH, GGKEme, NlfAgj) {
        EdpPKD = NmbiKM(EdpPKD);
        if (EdpPKD < 0 || EdpPKD > apKgiH.length - 1) {
            $error(17992881);
            return;
        };
        GmbBoJ = NmbiKM(GmbBoJ);
        fabDgH = NmbiKM(fabDgH);
        GGKEme = NmbiKM(GGKEme);
        this.LlCjig = ejHLnG();
        this.FLJHLb = apKgiH[EdpPKD];
        this.bglKFc = NmbiKM(NlfAgj);
        var fOGnCG, pKaopF;
        this.iEJHDn(0);
        this.inoPPG();
        this.DJafbE();
        this.ojjAHN();
        this.CipCaF.nbpblG();
        this.JENiKa = false;
        this.cnaFhk = false;
        var nApCaC = this.FLJHLb.eaGHGh;
        if (nApCaC < 0 || nApCaC > MnNneL.length - 1) {
            $error(68909385);
            return;
        };
        var BhKfLn = this.FLJHLb.gelDml;
        if (BhKfLn < 0 || BhKfLn > dagePF.length - 1) {
            $error(40991801);
            return;
        };
        var afcGdd = dagePF[BhKfLn];
        var McEjlk = this.LcdpGp.FeKiLh;
        McEjlk.table_framework.style.backgroundImage = 'url("' + BLAZE.nhjLnH.oAclpm('bitmap', 'billiards_framework_' + nApCaC).src + '")';
        McEjlk.table_base.style.backgroundImage = 'url("' + BLAZE.nhjLnH.oAclpm('bitmap', 'billiards_default_table').src + '")';
        this.ICNDka = MnNneL[nApCaC].jAnOai;
        this.DONAgB = {
            DaBjli: ecoKAl.NAkFIc(MnNneL[nApCaC].BNECAi),
            gCipfF: ecoKAl.NAkFIc(MnNneL[nApCaC].FgAmGe),
            eEmHpf: [MnNneL[nApCaC].kEKLHa[0], MnNneL[nApCaC].kEKLHa[1], Math.round(lJELmO.NImECF(MnNneL[nApCaC].kEKLHa[0], MnNneL[nApCaC].kEKLHa[1]) - JEpkfL)]
        };
        this.ebDANl = MnNneL[nApCaC].ekbEHn;
        this.LECdmi = MnNneL[nApCaC].IimcEf;
        this.bHBDje = MnNneL[nApCaC].Imlbnm;
        this.lMfbLD = MnNneL[nApCaC].JHiMkK;
        this.hacgoO = afcGdd.hJAPBi;
        this.oJPEMN = afcGdd.hJAPBi * dDFAkd;
        this.NmmCpf = this.oJPEMN * 2;
        if (this.bglKFc == 1) {
            this.pnkKjh = Math.round(this.FLJHLb.opIBcp * ibgFKk * dDFAkd);
            this.OfbJPI = Math.round(this.FLJHLb.fMHNgD * FEgCOl * dDFAkd);
            this.ocFimm = Math.round(this.FLJHLb.fMHNgD * cgCLNA * dDFAkd);
        } else {
            this.pnkKjh = Math.round(this.FLJHLb.opIBcp * dDFAkd);
            this.ocFimm = Math.round(this.FLJHLb.fMHNgD * dDFAkd);
        };
        this.pPCABE = Math.round(this.FLJHLb.NFpaah * dDFAkd);
        LIKAgg = this.NmmCpf;
        NgjbIn = this.NmmCpf * this.NmmCpf;
        this.njMdfO = {};
        this.pPGclC = [];
        var Mbamce = BLAZE.nhjLnH.oAclpm('bitmap', oHHiBg);
        var iEfGdl = (afcGdd.hJAPBi * 2) / 50;
        var Achpdo = ((afcGdd.hJAPBi * 2) / 40) - 0.02;
        var NpokeA = this.FLJHLb.pPGclC.clone();
        var HNOFJb = NpokeA.length;
        for (fOGnCG = 0; fOGnCG < HNOFJb; fOGnCG++) {
            pKaopF = NpokeA[fOGnCG];
            mhlkef = [pKaopF[0], 0, [0, 0], [0, 0], [1, 0], 0];
            var IjPpkB = afcGdd.pPGclC[pKaopF[1]];
            FcooBM = new BLAZE.BKaEgK(Mbamce, 1, 4, FiKoam);
            FcooBM.DMDNAD(iEfGdl);
            FcooBM.eHEgIc(0);
            this.CipCaF.mcnbao(-1, FcooBM);
            mhlkef.push(FcooBM);
            CJHGCK = new BLAZE.BKaEgK(Mbamce, 1, 4, FiKoam);
            CJHGCK.DMDNAD(iEfGdl);
            CJHGCK.eHEgIc(IjPpkB[0]);
            FcooBM.mcnbao(-1, CJHGCK);
            mhlkef.push(CJHGCK);
            if (IjPpkB[1] < 0) {
                mhlkef.push(null);
            } else {
                CJHGCK = new BLAZE.BKaEgK(BLAZE.nhjLnH.oAclpm('bitmap', 'billiards_ballanim_' + IjPpkB[1]), 1, 4, CiPeLK);
                CJHGCK.DMDNAD(Achpdo);
                CJHGCK.eHEgIc(HAELdp.mimoOg(0, IOKBHp - 1));
                CJHGCK.DAMlGi = HAELdp.mimoOg(0, 359);
                FcooBM.mcnbao(-1, CJHGCK);
                mhlkef.push(CJHGCK);
            };
            mhlkef.push(0);
            mhlkef.push(0);
            mhlkef.push(null);
            mhlkef.push([-1, -1, -1, -1, -1, -1, -1]);
            this.pPGclC.push(mhlkef);
            this.njMdfO['_' + mhlkef[0]] = fOGnCG;
            this.jMcjpd(mhlkef);
        };
        McEjlk.table_fabric.classList.remove('transition');
        McEjlk.table_fabric.style.backgroundImage = 'none';
        McEjlk.table_image.classList.remove('transition');
        McEjlk.table_image.style.backgroundImage = 'none';
        if (GmbBoJ > 0) {
            pKaopF = 'ttb' + GmbBoJ;
            BLAZE.nhjLnH.dkgJMA(pKaopF, PMFAbI + pKaopF + '.png?' + BLAZE.CONTENT_VERSION, 1, this.kgEkDP, this);
        };
        if (fabDgH > 0) {
            McEjlk.table_fabric.style.display = 'block';
            McEjlk.table_fabric.style.opacity = '0';
            pKaopF = 'fbr' + fabDgH;
            BLAZE.nhjLnH.dkgJMA(pKaopF, PMFAbI + pKaopF + '.png?' + BLAZE.CONTENT_VERSION, 1, this.hoFbeD, this);
        } else {
            McEjlk.table_fabric.style.display = 'none';
        };
        if (GGKEme > 0) {
            McEjlk.table_image.style.display = 'block';
            McEjlk.table_image.style.opacity = '0';
            pKaopF = 'tbg' + GGKEme;
            BLAZE.nhjLnH.dkgJMA(pKaopF, PMFAbI + pKaopF + '.png?' + BLAZE.CONTENT_VERSION, 1, this.eOgchp, this);
        } else {
            McEjlk.table_image.style.display = 'none';
        }
    };
    JpMdFf.prototype.bBliJe = function (NCHPmC) {
        this.NAdBAN = mPIIDJ.Aiipna(mLneaH.jfeJmo(NCHPmC));
        this.olhHil();
    };
    JpMdFf.prototype.olhHil = function () {
        var paOLfh = {};
        var AIfpLE = [];
        var NpokeA = this.FLJHLb.pPGclC.clone();
        var DILNMg, GOOiIp, fOGnCG, HNOFJb = NpokeA.length;
        var HolCMn = 0;
        for (fOGnCG = 0; fOGnCG < HNOFJb; fOGnCG++) {
            DILNMg = NpokeA.remove(this.NAdBAN[HolCMn] % NpokeA.length);
            GOOiIp = DILNMg[0];
            HolCMn++;
            if (HolCMn > 15) {
                HolCMn = 0;
            };
            mhlkef = this.kDBpDc(GOOiIp);
            AIfpLE.push(mhlkef);
            paOLfh['_' + GOOiIp] = fOGnCG;
        };
        this.pPGclC = AIfpLE;
        this.njMdfO = paOLfh;
    };
    JpMdFf.prototype.gIpBOH = function () {
        if (!this.FLJHLb) {
            $warn(97330684);
            return;
        };
        JMBDGp.gDicAB('table_setup', 1, false, 0, false);
        this.JENiKa = false;
        this.iEJHDn(0);
        var fOGnCG, mcipAh, pJIpGJ, CDKiOD;
        var kHEMgD = this.FLJHLb.kHEMgD * dDFAkd;
        var MiOMdj = kHEMgD * 2;
        var fGAOhL = this.FLJHLb.AgkCiF.clone();
        var jEHIEK = {};
        var JlNPcc = [];
        var NpokeA = this.FLJHLb.pPGclC;
        var HNOFJb = NpokeA.length;
        for (fOGnCG = 0; fOGnCG < HNOFJb; fOGnCG++) {
            mhlkef = NpokeA[fOGnCG];
            pJIpGJ = mhlkef[2];
            if (pJIpGJ >= 0) {
                jEHIEK['_' + mhlkef[0]] = fGAOhL[pJIpGJ];
                fGAOhL[pJIpGJ] = null;
            }
        };
        HNOFJb = fGAOhL.length;
        for (fOGnCG = 0; fOGnCG < HNOFJb; fOGnCG++) {
            if (fGAOhL[fOGnCG]) {
                JlNPcc.push(fGAOhL[fOGnCG]);
            }
        };
        var ifpaFO = [1, 1];
        var HNOFJb = this.pPGclC.length;
        var MiceiH = 0;
        for (fOGnCG = 0; fOGnCG < HNOFJb; fOGnCG++) {
            mhlkef = this.pPGclC[fOGnCG];
            FcooBM = mhlkef[6];
            CJHGCK = mhlkef[7];
            mhlkef[1] = 1;
            pJIpGJ = '_' + mhlkef[0];
            if (jEHIEK[pJIpGJ]) {
                lJELmO.cJJPaG(jEHIEK[pJIpGJ], mhlkef[2]);
            } else {
                mcipAh = JlNPcc.shift();
                lJELmO.cJJPaG(mcipAh, mhlkef[2]);
            };
            CDKiOD = Math.round(this.NAdBAN[MiceiH] / 2.55) * 0.01;
            MiceiH++;
            if (MiceiH > 15) {
                MiceiH = 0;
            };
            mhlkef[2][0] += (MiOMdj * CDKiOD) - kHEMgD;
            CDKiOD = Math.round(this.NAdBAN[MiceiH] / 2.55) * 0.01;
            MiceiH++;
            if (MiceiH > 15) {
                MiceiH = 0;
            };
            mhlkef[2][1] += (MiOMdj * CDKiOD) - kHEMgD;
            FcooBM.ifpaFO = ifpaFO;
            FcooBM.NhoOmg = 1;
            CJHGCK.NhoOmg = 1;
            mhlkef[3][0] = 0;
            mhlkef[3][1] = 0;
            mhlkef[5] = 0;
            if (mhlkef[8]) {
                mhlkef[8].NhoOmg = 1;
                mhlkef[8].eHEgIc(HAELdp.mimoOg(0, IOKBHp - 1));
                mhlkef[8].DAMlGi = HAELdp.mimoOg(0, 359);
            };
            mhlkef[9] = 0;
            mhlkef[10] = 0;
            mhlkef[11] = null;
            this.jMcjpd(mhlkef);
        };
        this.cnaFhk = false;
        this.CipCaF.aGcIfL();
    };
    JpMdFf.prototype.hcBGoK = function (MlomAd) {
        this.JENiKa = false;
        this.iEJHDn(0);
        var ifpaFO = [1, 1];
        var fOGnCG, HNOFJb = this.pPGclC.length;
        for (fOGnCG = 0; fOGnCG < HNOFJb; fOGnCG++) {
            mhlkef = this.pPGclC[fOGnCG];
            FcooBM = mhlkef[6];
            CJHGCK = mhlkef[7];
            mhlkef[1] = 0;
            FcooBM.ifpaFO = ifpaFO;
            FcooBM.NhoOmg = 1;
            CJHGCK.NhoOmg = 1;
            mhlkef[3][0] = 0;
            mhlkef[3][1] = 0;
            mhlkef[5] = 0;
            if (mhlkef[8]) {
                mhlkef[8].NhoOmg = 1;
            };
            mhlkef[9] = 0;
            mhlkef[10] = 0;
            mhlkef[11] = null;
        };
        HNOFJb = MlomAd.length;
        for (fOGnCG = 0; fOGnCG < HNOFJb; fOGnCG++) {
            var HIhniL = MlomAd[fOGnCG].split(';');
            if (HIhniL.length == 3) {
                mhlkef = this.kDBpDc(HIhniL[0]);
                if (mhlkef) {
                    mhlkef[1] = 1;
                    mhlkef[2][0] = mPIIDJ.llhDAb(HIhniL[1]);
                    mhlkef[2][1] = mPIIDJ.llhDAb(HIhniL[2]);
                } else {
                    $warn(12069251);
                }
            } else {
                $warn(12069252);
            }
        };
        HNOFJb = this.pPGclC.length;
        for (fOGnCG = 0; fOGnCG < HNOFJb; fOGnCG++) {
            this.jMcjpd(this.pPGclC[fOGnCG]);
        };
        this.cnaFhk = false;
        this.CipCaF.aGcIfL();
    };
    JpMdFf.prototype.HdnMpk = function (oKcffn, jJEIOG, NpokeA, BOfIMc) {
        if (!this.FLJHLb) {
            $warn(88029851);
            return;
        };
        jJEIOG = NmbiKM(jJEIOG);
        oKcffn = NmbiKM(oKcffn);
        var OPKHjd = this.kDBpDc(oKcffn);
        if (!OPKHjd) {
            $warn(88029852);
            return;
        };
        if (!OPKHjd[1]) {
            $warn(88029853);
            return;
        };
        var fOGnCG, HNOFJb;
        var ggJbPp = OPKHjd[2];
        var bmdKbj = NmbiKM(this.eAeFAO.NoCccJ);
        var afcGdd = null;
        if (NpokeA) {
            afcGdd = {};
            HNOFJb = NpokeA.length;
            for (var fOGnCG = 0; fOGnCG < HNOFJb; fOGnCG++) {
                afcGdd['_' + NpokeA[fOGnCG]] = true;
            }
        };
        var lnnAbF = null;
        if (BOfIMc) {
            lnnAbF = {};
            HNOFJb = BOfIMc.length;
            for (fOGnCG = 0; fOGnCG < HNOFJb; fOGnCG++) {
                lnnAbF['_' + BOfIMc[fOGnCG]] = true;
            }
        };
        var giFkbL = HAELdp.BObpdE(this.NmmCpf * 0.4);
        if (bmdKbj == 0) {
            fOGnCG = 0.18;
        } else if (bmdKbj == 1) {
            fOGnCG = 0.14;
        } else if (bmdKbj == 2) {
            fOGnCG = 0.09;
        };
        var lgoIep = HAELdp.BObpdE(this.NmmCpf - (dDFAkd * HAELdp.mimoOg(30, 100) * fOGnCG));
        var CdFJFI = [0, 0];
        var bIPBao = null;
        HNOFJb = this.pPGclC.length;
        for (fOGnCG = 0; fOGnCG < HNOFJb; fOGnCG++) {
            var doIlMd = this.pPGclC[fOGnCG];
            if (doIlMd[1]) {
                if (doIlMd[0] != oKcffn) {
                    if (afcGdd) {
                        if (!afcGdd['_' + doIlMd[0]]) {
                            continue;
                        }
                    };
                    lJELmO.cJJPaG(doIlMd[2], CdFJFI);
                    var IamPiO = lJELmO.NImECF(ggJbPp, CdFJFI);
                    for (var JNJBGk in this.LECdmi) {
                        if (lnnAbF) {
                            if (!lnnAbF[JNJBGk]) {
                                continue;
                            }
                        };
                        bIPBao = lJELmO.khOMcp(CdFJFI, this.LECdmi[JNJBGk]);
                        lJELmO.dbagEB(bIPBao);
                        lJELmO.dMdbkN(bIPBao, lgoIep);
                        lJELmO.jeDgdF(bIPBao, CdFJFI);
                        if (IamPiO - lJELmO.NImECF(ggJbPp, bIPBao) < giFkbL) {
                            continue;
                        };
                        if (this.KPkhia(ggJbPp, bIPBao, oKcffn, doIlMd[0])) {
                            continue;
                        };
                        if (this.KPkhia(bIPBao, this.LECdmi[JNJBGk], doIlMd[0], -1)) {
                            continue;
                        };
                        fOGnCG = HNOFJb;
                        break;
                    }
                };
            }
        };
        if (!bIPBao) {
            fOGnCG = giFkbL * 2;
            bIPBao = CdFJFI;
            if (bIPBao[0] == 0 && bIPBao[1] == 0) {
                bIPBao = lJELmO.FJPBMI();
                lJELmO.jeDgdF(bIPBao, ggJbPp);
            } else {
                lJELmO.jeDgdF(bIPBao, [HAELdp.mimoOg(0, fOGnCG) - giFkbL, HAELdp.mimoOg(0, fOGnCG) - giFkbL]);
            }
        };
        lJELmO.IFDeod(bIPBao, ggJbPp);
        lJELmO.dbagEB(bIPBao);
        lJELmO.dMdbkN(bIPBao, HAELdp.mimoOg(50, 100) * 0.01 * this.pnkKjh);
        this.BePFKa(oKcffn, bIPBao, [0, 0, 0], jJEIOG, 0, 1);
    };
    JpMdFf.prototype.BePFKa = function (oKcffn, MFICHO, ccgPCC, jJEIOG, nILmCh, IJOPAi) {
        if (!this.FLJHLb) {
            $warn(57239481);
            return;
        };
        mhlkef = this.kDBpDc(oKcffn);
        if (!mhlkef) {
            $warn(57239482);
            return;
        };
        if (!mhlkef[1]) {
            $warn(57239483);
            return;
        };
        this.DJafbE();
        this.AIIHhG.HjGcOh();
        this.aeIOMF = oKcffn;
        this.KKmlPp = 0;
        this.jMpMAo = 0;
        this.NjCJMh();
        if (ccgPCC[0] < -1000) {
            ccgPCC[0] = -1000;
        } else if (ccgPCC[0] > 1000) {
            ccgPCC[0] = 1000;
        };
        if (ccgPCC[1] < -1000) {
            ccgPCC[1] = -1000;
        } else if (ccgPCC[1] > 1000) {
            ccgPCC[1] = 1000;
        };
        if (ccgPCC[2] < -1000) {
            ccgPCC[2] = -1000;
        } else if (ccgPCC[2] > 1000) {
            ccgPCC[2] = 1000;
        };
        var fAEidE = ccgPCC.clone();
        if (fAEidE[0] == 0 && fAEidE[1] == 0 && fAEidE[2] == 0) {
            mhlkef[11] = null;
        } else {
            lJELmO.dbagEB(fAEidE);
            mhlkef[11] = fAEidE;
            mhlkef[11][2] = mhlkef[11][2] * fAEidE[0] * 0.00006;
            mhlkef[11][3] = lJELmO.hIoKBj([0, 0], fAEidE);
        };
        lJELmO.BObpdE(MFICHO);
        lJELmO.cJJPaG(MFICHO, mhlkef[3]);
        lJELmO.cJJPaG(mhlkef[3], mhlkef[4]);
        lJELmO.dbagEB(mhlkef[4]);
        mhlkef[5] = HAELdp.BObpdE(lJELmO.PaaKha(mhlkef[3]));
        if (mhlkef[5] > this.pnkKjh) {
            mhlkef[5] = this.pnkKjh;
            lJELmO.cJJPaG(mhlkef[4], mhlkef[3]);
            lJELmO.dMdbkN(mhlkef[3], mhlkef[5]);
        };
        if (mhlkef[8]) {
            mhlkef[8].DAMlGi = lJELmO.hgngnB(mhlkef[4]);
        };
        this.MDfoNP(oKcffn, jJEIOG, nILmCh, true);
        if (IJOPAi > 0) {
            this.JENiKa = true;
            this.JgOAFb.classList.add('autodist');
            window.setTimeout(this.EdPaNN, 400, [this, mhlkef[5]]);
            window.setTimeout(this.LJOPPP, 400, this);
            this.dodcjj = lJELmO.PaaKha(MFICHO) / this.pnkKjh;
            if (this.dodcjj < ooFOBc) {
                this.dodcjj = ooFOBc;
            };
            this.bKclpB();
        } else {
            this.JENiKa = false;
            this.eCMpjp('dchiKB', mhlkef[5]);
            this.iEJHDn(HOKnla);
            this.JgOAFb.classList.remove('autodist');
            this.cnaFhk = true;
            this.iNbfnE.style.top = HAELdp.BObpdE(this.GJCkgG * (this.hacgoO - 5)) + 'px';
        };
        var emKbHd = lJELmO.NoeNdn(mhlkef[2]);
        var gOHGOp = lJELmO.mCMKjO(emKbHd, mhlkef[3]);
        if (this.BkoHcI.hPEEGo) {
            var fOGnCG = emKbHd[1];
            emKbHd[1] = GdeJPB[1] - emKbHd[0];
            emKbHd[0] = fOGnCG;
            fOGnCG = gOHGOp[1];
            gOHGOp[1] = GdeJPB[1] - gOHGOp[0];
            gOHGOp[0] = fOGnCG;
            this.maIOaI = lJELmO.hIoKBj(gOHGOp, emKbHd);
        } else {
            this.maIOaI = lJELmO.hIoKBj(emKbHd, gOHGOp);
        };
        this.BdimnP = false;
        ggGkJc.nKCAoj(this.JgOAFb, this.maIOaI);
        if (IJOPAi == 0 || IJOPAi == 1) {
            this.AIIHhG.DJMNpK({
                c: 'shot',
                v: [oKcffn, mPIIDJ.kNAikO(mhlkef[2][0], 0), mPIIDJ.kNAikO(mhlkef[2][1], 0), MFICHO[0], MFICHO[1], ccgPCC[0], ccgPCC[1], ccgPCC[2]].join(':')
            });
        }
    };
    JpMdFf.prototype.EdPaNN = function (MKjgcC) {
        if (!MKjgcC) {
            return;
        };
        MKjgcC[0].eCMpjp('dchiKB', MKjgcC[1]);
    };
    JpMdFf.prototype.LJOPPP = function (pMdaFp) {
        if (!pMdaFp.JENiKa) {
            return;
        };
        pMdaFp.iEJHDn(HOKnla);
        pMdaFp.JgOAFb.classList.remove('autodist');
        pMdaFp.JENiKa = false;
        pMdaFp.cnaFhk = true;
        pMdaFp.iNbfnE.style.top = HAELdp.BObpdE(pMdaFp.GJCkgG * (pMdaFp.hacgoO - 5)) + 'px';
    };
    JpMdFf.prototype.kDBpDc = function (oKcffn) {
        oKcffn = NmbiKM(oKcffn);
        beBjbj = this.njMdfO['_' + oKcffn];
        if (beBjbj === undefined) {
            $warn(49005901);
            return null;
        };
        mhlkef = this.pPGclC[beBjbj];
        if (mhlkef[0] != oKcffn) {
            $warn(49005902);
            return null;
        };
        return mhlkef;
    };
    JpMdFf.prototype.NjCJMh = function () {
        if (this.cnaFhk) {
            $warn(60297738);
        };
        var aJgneA, HNOFJb = this.pPGclC.length;
        for (var fOGnCG = 0; fOGnCG < HNOFJb; fOGnCG++) {
            aJgneA = this.pPGclC[fOGnCG][12];
            aJgneA[0] = -1;
            aJgneA[1] = -1;
            aJgneA[2] = -1;
            aJgneA[3] = -1;
            aJgneA[4] = -1;
            aJgneA[5] = -1;
            aJgneA[6] = -1;
        }
    };
    JpMdFf.prototype.NKeAKN = function () {
        return (ejHLnG() - this.LlCjig) < 1000;
    };
    JpMdFf.prototype.oackNC = function (BiAKPf, aCKfgg, pMdaFp) {
        if (!pMdaFp) {
            return;
        };
        if (!pMdaFp.gAhNem) {
            return;
        };
        if (aCKfgg && !pMdaFp.gAhNem[BiAKPf]) {
            pMdaFp.gAhNem[BiAKPf] = 'url("' + aCKfgg.src + '")';
            if (pMdaFp.eAAjjm > 0) {
                if (pMdaFp.lPColI === BiAKPf) {
                    pMdaFp.EJeBcH.style.backgroundImage = pMdaFp.gAhNem[BiAKPf];
                    if (BiAKPf.substring(0, 4) == 'acue') {
                        pMdaFp.EJeBcH.classList.add('sprite');
                        pMdaFp.JNGiGP.style.backgroundImage = pMdaFp.gAhNem[BiAKPf];
                        var plbgkl = BjmnkM[NmbiKM(BiAKPf.substring(4))];
                        pMdaFp.JNGiGP.style.top = plbgkl[0] + '%';
                        pMdaFp.JNGiGP.style.bottom = (100 - plbgkl[0] - 50) + '%';
                        hkdcJB.ogbElm(pMdaFp.JNGiGP, plbgkl[3], plbgkl[1], plbgkl[2]);
                    } else {
                        pMdaFp.EJeBcH.classList.remove('sprite');
                        pMdaFp.JNGiGP.style.backgroundImage = '';
                        hkdcJB.EopacH(pMdaFp.JNGiGP, true);
                    }
                };
            }
        };
    };
    JpMdFf.prototype.kgEkDP = function (BiAKPf, aCKfgg, pMdaFp) {
        if (!pMdaFp || !aCKfgg) {
            return;
        };
        if (!pMdaFp.LcdpGp) {
            return;
        };
        var IgMlEF = pMdaFp.LcdpGp.FeKiLh.table_base;
        IgMlEF.style.backgroundImage = 'url("' + aCKfgg.src + '")';
    };
    JpMdFf.prototype.hoFbeD = function (BiAKPf, aCKfgg, pMdaFp) {
        if (!pMdaFp || !aCKfgg) {
            return;
        };
        if (!pMdaFp.LcdpGp) {
            return;
        };
        var IgMlEF = pMdaFp.LcdpGp.FeKiLh.table_fabric;
        IgMlEF.style.backgroundImage = 'url("' + aCKfgg.src + '")';
        if (!pMdaFp.NKeAKN()) {
            IgMlEF.classList.add('transition');
        };
        IgMlEF.style.opacity = '1';
    };
    JpMdFf.prototype.eOgchp = function (BiAKPf, aCKfgg, pMdaFp) {
        if (!pMdaFp || !aCKfgg) {
            return;
        };
        if (!pMdaFp.LcdpGp) {
            return;
        };
        var IgMlEF = pMdaFp.LcdpGp.FeKiLh.table_image;
        IgMlEF.style.backgroundImage = 'url("' + aCKfgg.src + '")';
        if (!pMdaFp.NKeAKN()) {
            IgMlEF.classList.add('transition');
        };
        IgMlEF.style.opacity = '1';
    };
    JpMdFf.prototype.ADEEjn = function () {
        var FOJpbB = false;
        var fOGnCG, LfEFlm, HNOFJb = this.pPGclC.length;
        for (fOGnCG = 0; fOGnCG < HNOFJb; fOGnCG++) {
            LfEFlm = this.pPGclC[fOGnCG];
            if (this.APGELP(LfEFlm)) {
                FOJpbB = true;
            }
        };
        if (FOJpbB) {
            this.CipCaF.aGcIfL();
        } else if (this.cnaFhk) {
            if (this.eAeFAO.jHIGoB) {
                var aJgneA;
                var bjMBcI = {};
                bjMBcI.a = this.aeIOMF;
                var KmngMC = this.BJoBNk[1];
                if (KmngMC == 'carom') {
                    mhlkef = this.kDBpDc(0);
                    if (mhlkef[1] == 1) {
                        aJgneA = mhlkef[12];
                        if (aJgneA[0] > 0) {
                            if (aJgneA[4] == 0) {
                                mhlkef = this.kDBpDc(1);
                                if (mhlkef[12][5] == 1) {
                                    mhlkef = this.kDBpDc(2);
                                    if (mhlkef[12][5] == 1) {
                                        this.KKmlPp = 1;
                                    }
                                };
                            }
                        };
                    }
                } else if (KmngMC == 'bank') {
                    mhlkef = this.kDBpDc(0);
                    if (mhlkef[1] == 1) {
                        aJgneA = mhlkef[12];
                        if (aJgneA[0] > 0) {
                            Nhgpna = this.kDBpDc(aJgneA[0]);
                            if (Nhgpna) {
                                if (Nhgpna[1] != 1 && Nhgpna[12][1] == 1) {
                                    this.KKmlPp = aJgneA[0];
                                }
                            };
                        }
                    };
                } else if (KmngMC == 'scoreball') {
                    mhlkef = this.kDBpDc(0);
                    if (mhlkef[1] == 1) {
                        aJgneA = mhlkef[12][6];
                        if (aJgneA == 23 || aJgneA == 7) {
                            this.KKmlPp = 1;
                        } else if (aJgneA == 6 || aJgneA == 24 || aJgneA == 22 || aJgneA == 8) {
                            this.KKmlPp = 2;
                        }
                    };
                };
                if (this.KKmlPp > 0) {
                    bjMBcI.s = this.KKmlPp;
                };
                var InIPKb = [];
                for (fOGnCG = 0; fOGnCG < HNOFJb; fOGnCG++) {
                    mhlkef = this.pPGclC[fOGnCG];
                    aJgneA = mhlkef[12];
                    if (mhlkef[1] == 1) {
                        NOAbGk = mhlkef[2];
                        InIPKb.push([mhlkef[0], aJgneA[0], mPIIDJ.kNAikO(NOAbGk[0], 0), mPIIDJ.kNAikO(NOAbGk[1], 0)].join('#'));
                    } else if (aJgneA[2] >= 0) {
                        InIPKb.push([mhlkef[0], aJgneA[0], aJgneA[2], aJgneA[3], ''].join('#'));
                    }
                };
                bjMBcI.b = InIPKb.join('|');
                this.AIIHhG.DJMNpK({
                    c: 'pres',
                    v: bjMBcI
                });
            };
            this.CipCaF.aGcIfL();
            this.cnaFhk = false;
            this.cFaPCi();
        }
    };
    JpMdFf.prototype.APGELP = function (OPKHjd) {
        if (OPKHjd[1] != 1) {
            if (OPKHjd[10] <= 0) {
                return false;
            };
            OPKHjd[10] -= 1;
            this.jMcjpd(OPKHjd);
            return true;
        };
        lKclNn = OPKHjd[5];
        if (lKclNn <= 0) {
            return false;
        };
        fLoOmD = OPKHjd[3];
        if (lKclNn <= 0) {
            OPKHjd[11] = null;
            OPKHjd[5] = 0;
            fLoOmD[0] = 0;
            fLoOmD[1] = 0;
            BLAZE.bacjNj.BkhDDo(OPKHjd[0]);
            return false;
        };
        CJHGCK = OPKHjd[8];
        if (CJHGCK) {
            GIgPag = HAELdp.BObpdE(OPKHjd[9] + lKclNn);
            OdjMli = GIgPag % abMndG;
            GIgPag = (GIgPag - OdjMli) / abMndG;
            OPKHjd[9] = OdjMli;
            if (GIgPag > 0) {
                CJHGCK.eHEgIc(CJHGCK.nEEMOI() + GIgPag);
            } else {
                if (OPKHjd[10] == 0) {
                    OPKHjd[10] = 1;
                } else {
                    OPKHjd[10] = 0;
                    OPKHjd[9] = 0;
                    CJHGCK.eHEgIc(CJHGCK.nEEMOI() + 1);
                }
            };
        };
        lJELmO.cJJPaG(OPKHjd[4], fLoOmD);
        lJELmO.dMdbkN(fLoOmD, lKclNn);
        NOAbGk = OPKHjd[2];
        dgcnik = lJELmO.mCMKjO(NOAbGk, fLoOmD);
        jGhjGb = [0];
        fBfhIC = 99999999;
        bgLEIF = this.lMfbLD[this.mgHfFI(NOAbGk)][this.mgHfFI(dgcnik)];
        if (bgLEIF) {
            GIgPag = bgLEIF.length;
            for (OdjMli = 0; OdjMli < GIgPag; OdjMli++) {
                KmkHIm = this.fAOhnI(bgLEIF[OdjMli]);
                HnPGCc = this.japcEB(NOAbGk, dgcnik, KmkHIm[0], KmkHIm[1]);
                if (HnPGCc) {
                    EDdliE = lJELmO.NImECF(NOAbGk, HnPGCc) - dDFAkd;
                    if (EDdliE < 0) {
                        EDdliE = 0;
                    };
                    if (fBfhIC > EDdliE) {
                        fBfhIC = EDdliE;
                        jGhjGb[0] = 1;
                        jGhjGb[1] = KmkHIm[0];
                        jGhjGb[2] = KmkHIm[1];
                        jGhjGb[3] = EDdliE;
                        jGhjGb[4] = bgLEIF[OdjMli];
                        jGhjGb[5] = HnPGCc;
                    }
                };
            }
        };
        hFNgFN = OPKHjd[0];
        kmHOGk = lKclNn + this.NmmCpf + CGMpPj;
        bJefno = this.pPGclC;
        GIgPag = bJefno.length;
        for (OdjMli = 0; OdjMli < GIgPag; OdjMli++) {
            Nhgpna = bJefno[OdjMli];
            if (Nhgpna[1]) {
                if (Nhgpna[0] != hFNgFN) {
                    KmkHIm = this.EgAJnM(fBfhIC, NOAbGk, dgcnik, fLoOmD, lKclNn, Nhgpna[2], Nhgpna[3]);
                    if (KmkHIm) {
                        fBfhIC = KmkHIm[0];
                        jGhjGb[0] = 2;
                        jGhjGb[1] = KmkHIm;
                        jGhjGb[2] = Nhgpna;
                    }
                };
            }
        };
        if (jGhjGb[0] == 1) {
            if (jGhjGb[1][2] > 0) {
                this.eCMpjp('NEeGOB', lKclNn);
                dgcnik = this.AImpEM(jGhjGb[1][2]);
                BLAZE.bacjNj.DNOoBc(hFNgFN, dgcnik);
                lJELmO.BObpdE(dgcnik);
                lJELmO.cJJPaG(dgcnik, NOAbGk);
                OPKHjd[11] = null;
                OPKHjd[1] = 0;
                OPKHjd[5] = 0;
                lKclNn = 0;
                OPKHjd[10] = DgiCNk;
                fLoOmD[0] = 0;
                fLoOmD[1] = 0;
                KmkHIm = OPKHjd[6].AcPOPM;
                lJELmO.cJJPaG(OPKHjd[2], KmkHIm);
                lJELmO.dMdbkN(KmkHIm, ljLfNo);
                OPKHjd[12][2] = this.jMpMAo;
                OPKHjd[12][3] = jGhjGb[1][2];
                this.jMpMAo++;
            } else {
                if (OPKHjd[12][0] < 0) {
                    if (OPKHjd[12][6] < 0) {
                        OPKHjd[12][6] = jGhjGb[4];
                    }
                };
                if (OPKHjd[12][1] < 0) {
                    if (jGhjGb[1][0] == jGhjGb[2][0]) {
                        OPKHjd[12][1] = 1;
                    } else if (jGhjGb[1][1] == jGhjGb[2][1]) {
                        OPKHjd[12][1] = 1;
                    }
                };
                if (OPKHjd[12][4] < 0) {
                    if (OPKHjd[12][0] >= 0) {
                        OPKHjd[12][4] = 0;
                    }
                };
                this.eCMpjp('EPAaHk', lKclNn);
                if (OPKHjd[11]) {
                    if (OPKHjd[11][0] != 0) {
                        OPKHjd[11][0] = 0;
                    };
                    if (OPKHjd[11][1] != 0) {
                        OPKHjd[11][1] = 0;
                    }
                };
                dgcnik = lJELmO.NoeNdn(OPKHjd[4]);
                lJELmO.dMdbkN(dgcnik, jGhjGb[3]);
                lJELmO.jeDgdF(dgcnik, NOAbGk);
                BLAZE.bacjNj.khgDLh(hFNgFN, dgcnik, jGhjGb[5], lKclNn);
                this.PDahGf(OPKHjd, jGhjGb[1], jGhjGb[2]);
                lKclNn = lKclNn - this.pPCABE;
                if (lKclNn <= 0) {
                    lKclNn = 0;
                    fLoOmD[0] = 0;
                    fLoOmD[1] = 0;
                } else {
                    lJELmO.cJJPaG(OPKHjd[4], fLoOmD);
                    lJELmO.dMdbkN(fLoOmD, lKclNn);
                    lJELmO.BObpdE(fLoOmD);
                }
            };
        } else if (jGhjGb[0] == 2) {
            PoeeGO = lKclNn;
            KmkHIm = jGhjGb[1];
            dgcnik = KmkHIm[1];
            if (OPKHjd[11]) {
                EObkea = lKclNn;
                ipgmHM = lJELmO.NoeNdn(OPKHjd[4]);
            };
            lJELmO.cJJPaG(KmkHIm[2], fLoOmD);
            lJELmO.BObpdE(fLoOmD);
            lJELmO.cJJPaG(fLoOmD, OPKHjd[4]);
            lJELmO.dbagEB(OPKHjd[4]);
            lKclNn = HAELdp.BObpdE(lJELmO.PaaKha(fLoOmD));
            if (OPKHjd[11]) {
                if (OPKHjd[11][0] != 0 || OPKHjd[11][1] != 0) {
                    EPJHkf = lKclNn / EObkea;
                    lKclNn = lKclNn * 0.4 + (EObkea * lJELmO.PaaKha(OPKHjd[11]) * (1 - EPJHkf) * 0.4);
                    lJELmO.dMdbkN(OPKHjd[4], EPJHkf);
                    lJELmO.Ihonom(ipgmHM, OPKHjd[11][3]);
                    lJELmO.dMdbkN(ipgmHM, 1 - EPJHkf);
                    lJELmO.jeDgdF(OPKHjd[4], ipgmHM);
                    lJELmO.dbagEB(OPKHjd[4]);
                    lJELmO.cJJPaG(OPKHjd[4], fLoOmD);
                    lJELmO.dMdbkN(fLoOmD, lKclNn);
                    lJELmO.BObpdE(fLoOmD);
                    OPKHjd[11][0] = 0;
                    OPKHjd[11][1] = 0;
                }
            };
            if (OPKHjd[8]) {
                if (lKclNn > dDFAkd) {
                    OPKHjd[8].DAMlGi = lJELmO.hgngnB(OPKHjd[4]);
                }
            };
            Nhgpna = jGhjGb[2];
            if (Nhgpna[11]) {
                EObkea = Nhgpna[5];
                ipgmHM = lJELmO.NoeNdn(Nhgpna[4]);
            };
            lJELmO.cJJPaG(KmkHIm[3], Nhgpna[3]);
            lJELmO.BObpdE(Nhgpna[3]);
            lJELmO.cJJPaG(Nhgpna[3], Nhgpna[4]);
            lJELmO.dbagEB(Nhgpna[4]);
            Nhgpna[5] = HAELdp.BObpdE(lJELmO.PaaKha(Nhgpna[3]));
            if (Nhgpna[11]) {
                if (Nhgpna[11][0] != 0 || Nhgpna[11][1] != 0) {
                    EPJHkf = Nhgpna[5] / EObkea;
                    Nhgpna[5] = Nhgpna[5] * 0.4 + (EObkea * lJELmO.PaaKha(Nhgpna[11]) * (1 - EPJHkf) * 0.4);
                    lJELmO.dMdbkN(Nhgpna[4], EPJHkf);
                    lJELmO.Ihonom(ipgmHM, Nhgpna[11][3]);
                    lJELmO.dMdbkN(ipgmHM, 1 - EPJHkf);
                    lJELmO.jeDgdF(Nhgpna[4], ipgmHM);
                    lJELmO.dbagEB(Nhgpna[4]);
                    lJELmO.cJJPaG(Nhgpna[4], Nhgpna[3]);
                    lJELmO.dMdbkN(Nhgpna[3], Nhgpna[5]);
                    lJELmO.BObpdE(Nhgpna[3]);
                    Nhgpna[11][0] = 0;
                    Nhgpna[11][1] = 0;
                }
            };
            if (Nhgpna[8]) {
                if (Nhgpna[5] > dDFAkd) {
                    Nhgpna[8].DAMlGi = lJELmO.hgngnB(Nhgpna[4]);
                }
            };
            if (lKclNn > Nhgpna[5]) {
                this.eCMpjp('OPKHjd', lKclNn);
            } else {
                this.eCMpjp('OPKHjd', Nhgpna[5]);
            };
            if (OPKHjd[12][4] < 0) {
                if (OPKHjd[12][0] >= 0) {
                    OPKHjd[12][4] = 1;
                }
            };
            if (Nhgpna[12][4] < 0) {
                if (Nhgpna[12][0] >= 0) {
                    Nhgpna[12][4] = 1;
                }
            };
            if (OPKHjd[12][0] < 0) {
                OPKHjd[12][0] = Nhgpna[0];
            };
            if (Nhgpna[12][0] < 0) {
                Nhgpna[12][0] = OPKHjd[0];
            };
            if (Nhgpna[0] == 0) {
                OPKHjd[12][5] = 1;
            };
            if (OPKHjd[0] == 0) {
                Nhgpna[12][5] = 1;
            };
            BLAZE.bacjNj.JcFmhK(hFNgFN, dgcnik, Nhgpna[0], Nhgpna[2], PoeeGO);
        };
        if (OPKHjd[1]) {
            BLAZE.bacjNj.OJffen(hFNgFN, NOAbGk, dgcnik, lKclNn);
        };
        lJELmO.BObpdE(dgcnik);
        lJELmO.cJJPaG(dgcnik, NOAbGk);
        if (OPKHjd[11]) {
            lJELmO.Ihonom(OPKHjd[4], OPKHjd[11][2] * (lKclNn / this.pnkKjh));
            lJELmO.dbagEB(OPKHjd[4]);
            lJELmO.cJJPaG(OPKHjd[4], fLoOmD);
            lJELmO.dMdbkN(fLoOmD, lKclNn);
            lJELmO.BObpdE(fLoOmD);
        };
        if (this.bglKFc == 1) {
            lKclNn = HAELdp.BObpdE(lKclNn - (this.ocFimm + ((lKclNn / this.pnkKjh) * this.OfbJPI)));
        } else {
            lKclNn = HAELdp.BObpdE(lKclNn - this.ocFimm);
        };
        OPKHjd[5] = lKclNn;
        if (OPKHjd[1]) {
            if (lKclNn <= 0) {
                BLAZE.bacjNj.BkhDDo(hFNgFN);
            }
        };
        this.jMcjpd(OPKHjd);
        return true;
    };
    JpMdFf.prototype.jMcjpd = function (OPKHjd) {
        FcooBM = OPKHjd[6];
        CJHGCK = OPKHjd[7];
        if (OPKHjd[1] != 1) {
            if (OPKHjd[10] > 0) {
                if (!FcooBM.HilidP) {
                    FcooBM.HilidP = true;
                };
                GIgPag = OPKHjd[10];
                OdjMli = FknbkJ + ((GIgPag - 1) * eLiahC);
                FcooBM.ifpaFO = [OdjMli, OdjMli];
                OdjMli = iMgPoP * GIgPag;
                FcooBM.NhoOmg = OdjMli;
                CJHGCK.NhoOmg = OdjMli;
                CJHGCK = OPKHjd[8];
                if (CJHGCK) {
                    CJHGCK.NhoOmg = OdjMli;
                }
            } else if (FcooBM.HilidP) {
                FcooBM.HilidP = false;
            }
        } else {
            if (!FcooBM.HilidP) {
                FcooBM.HilidP = true;
            };
            NOAbGk = FcooBM.AcPOPM;
            lJELmO.cJJPaG(OPKHjd[2], NOAbGk);
            lJELmO.dMdbkN(NOAbGk, ljLfNo);
        }
    };
    JpMdFf.prototype.mgHfFI = function (AcPOPM) {
        if (AcPOPM[0] < 0) {
            AcPOPM = [0, AcPOPM[1]];
        } else if (AcPOPM[0] >= GdeJPB[0]) {
            AcPOPM = [GdeJPB[0] - dDFAkd, AcPOPM[1]];
        };
        if (AcPOPM[1] < 0) {
            AcPOPM = [AcPOPM[0], 0];
        } else if (AcPOPM[1] >= GdeJPB[1]) {
            AcPOPM = [AcPOPM[0], GdeJPB[1] - dDFAkd];
        };
        return HAELdp.OHokFB(AcPOPM[0] / nFhIkg[0]) + HAELdp.OHokFB(AcPOPM[1] / nFhIkg[1]) * EeJJiE[0];
    };
    JpMdFf.prototype.fAOhnI = function (NLhAgd) {
        return [this.bHBDje[NLhAgd], this.bHBDje[NLhAgd + 1]];
    };
    JpMdFf.prototype.AImpEM = function (FGoAob) {
        var DILNMg = this.ebDANl['_' + FGoAob];
        if (!DILNMg) {
            DILNMg = [0, 0];
        };
        return DILNMg;
    };
    JpMdFf.prototype.japcEB = function (bocKCp, gNdblD, AEPHMl, PEIeNj) {
        OOfOEh = gNdblD[1] - bocKCp[1];
        imfodK = bocKCp[0] - gNdblD[0];
        cCJPfc = AEPHMl[3];
        pdOcjk = AEPHMl[4];
        danOlm = (OOfOEh * pdOcjk) - (cCJPfc * imfodK);
        if (Math.abs(danOlm) == 0) {
            return null;
        };
        PAHapA = bocKCp[0] - AEPHMl[0];
        mFcNma = bocKCp[1] - AEPHMl[1];
        nfGFPn = PAHapA * cCJPfc - mFcNma * (PEIeNj[0] - AEPHMl[0]);
        kOPFmM = nfGFPn / -danOlm;
        if (kOPFmM < 0 || kOPFmM > 1) {
            return null;
        };
        angnGb = mFcNma * imfodK - PAHapA * (bocKCp[1] - gNdblD[1]);
        KhnHoD = angnGb / -danOlm;
        if (KhnHoD < 0 || KhnHoD > 1) {
            return null;
        };
        kcJokA = (gNdblD[0] * bocKCp[1]) - (bocKCp[0] * gNdblD[1]);
        heOOOB = AEPHMl[5];
        return [((imfodK * heOOOB) - (pdOcjk * kcJokA)) / danOlm, ((cCJPfc * kcJokA) - (OOfOEh * heOOOB)) / danOlm];
    };
    JpMdFf.prototype.PDahGf = function (OPKHjd, BLBLFH, jmdnOK) {
        nfGFPn = OPKHjd[3];
        angnGb = BLBLFH[6];
        PAHapA = jmdnOK[0] - BLBLFH[0];
        mFcNma = jmdnOK[1] - BLBLFH[1];
        kcJokA = -mFcNma / angnGb;
        heOOOB = PAHapA / angnGb;
        danOlm = -nfGFPn[0] * kcJokA - nfGFPn[1] * heOOOB;
        OPKHjd[3][0] = nfGFPn[0] + 2 * kcJokA * danOlm;
        OPKHjd[3][1] = nfGFPn[1] + 2 * heOOOB * danOlm;
        lJELmO.BObpdE(OPKHjd[3]);
        lJELmO.cJJPaG(OPKHjd[3], OPKHjd[4]);
        lJELmO.dbagEB(OPKHjd[4]);
        OPKHjd[5] = HAELdp.BObpdE(lJELmO.PaaKha(OPKHjd[3]));
        if (OPKHjd[8]) {
            if (OPKHjd[5] > dDFAkd) {
                OPKHjd[8].DAMlGi = lJELmO.hgngnB(OPKHjd[4]);
            }
        };
    };
    JpMdFf.prototype.iaGfJl = function (hjAIdB, BLBLFH, jmdnOK) {
        angnGb = BLBLFH[6];
        PAHapA = jmdnOK[0] - BLBLFH[0];
        mFcNma = jmdnOK[1] - BLBLFH[1];
        kcJokA = -mFcNma / angnGb;
        heOOOB = PAHapA / angnGb;
        danOlm = -hjAIdB[0] * kcJokA - hjAIdB[1] * heOOOB;
        nfGFPn = [hjAIdB[0] + 2 * kcJokA * danOlm, hjAIdB[1] + 2 * heOOOB * danOlm];
        lJELmO.dbagEB(nfGFPn);
        return nfGFPn;
    };
    JpMdFf.prototype.EgAJnM = function (ifooFf, GoPLPc, dgdnIJ, EkDLdo, NAoNiO, MoLpoB, PcIpLO) {
        hHgcCD = lJELmO.hIoKBj(GoPLPc, MoLpoB) - lJELmO.IHmieI(EkDLdo);
        NdGnPG = lJELmO.NImECF(GoPLPc, MoLpoB);
        HkAGdB = Math.sin(hHgcCD) * NdGnPG;
        if (HkAGdB <= 0) {
            return null;
        };
        if (HkAGdB >= NAoNiO) {
            if (HkAGdB >= NAoNiO + LIKAgg) {
                return null;
            };
            if (lJELmO.NImECF(dgdnIJ, MoLpoB) > LIKAgg) {
                return null;
            }
        };
        cnoMOg = Math.abs(Math.cos(hHgcCD) * NdGnPG);
        if (cnoMOg >= LIKAgg) {
            return null;
        };
        OdpkmM = Math.sqrt(NgjbIn - cnoMOg * cnoMOg) - CGMpPj;
        if (OdpkmM > HkAGdB || OdpkmM < 0) {
            OdpkmM = 0;
        } else {
            OdpkmM = HkAGdB - OdpkmM;
        };
        if (ifooFf < OdpkmM) {
            return null;
        };
        if (NAoNiO > 0 && OdpkmM > 0) {
            lBlIhb = lJELmO.NoeNdn(EkDLdo);
            lJELmO.dMdbkN(lBlIhb, (1.0 / NAoNiO) * OdpkmM);
            IedkAJ = lJELmO.mCMKjO(GoPLPc, lBlIhb);
        } else {
            IedkAJ = lJELmO.NoeNdn(GoPLPc);
        };
        ipgmHM = lJELmO.khOMcp(MoLpoB, IedkAJ);
        lJELmO.ibGKip(ipgmHM);
        lJELmO.HpDGlG(ipgmHM, LIKAgg);
        lJELmO.dMdbkN(ipgmHM, (EkDLdo[0] - PcIpLO[0]) * ipgmHM[0] + (EkDLdo[1] - PcIpLO[1]) * ipgmHM[1]);
        return [OdpkmM, IedkAJ, lJELmO.khOMcp(EkDLdo, ipgmHM), lJELmO.mCMKjO(PcIpLO, ipgmHM)];
    };
    JpMdFf.prototype.KPkhia = function (miaLml, odJCjO, MIKkAO, GNkDag) {
        var fOGnCG, OPKHjd, HNOFJb = this.pPGclC.length;
        for (fOGnCG = 0; fOGnCG < HNOFJb; fOGnCG++) {
            OPKHjd = this.pPGclC[fOGnCG];
            if (OPKHjd[1]) {
                if (OPKHjd[0] != MIKkAO && OPKHjd[0] != GNkDag) {
                    if (this.BMOIpc(miaLml, odJCjO, OPKHjd[2])) {
                        return true;
                    }
                };
            }
        };
        return false;
    };
    JpMdFf.prototype.BMOIpc = function (MCIkbK, lbOdHO, PhpjBi) {
        ipgmHM = lJELmO.khOMcp(lbOdHO, MCIkbK);
        fLoOmD = lJELmO.PaaKha(ipgmHM);
        hHgcCD = lJELmO.hIoKBj(MCIkbK, PhpjBi) - lJELmO.IHmieI(ipgmHM);
        NdGnPG = lJELmO.NImECF(MCIkbK, PhpjBi);
        HkAGdB = Math.sin(hHgcCD) * NdGnPG;
        if (HkAGdB <= 0) {
            return false;
        };
        if (HkAGdB >= fLoOmD) {
            if (HkAGdB >= fLoOmD + LIKAgg) {
                return false;
            };
            if (lJELmO.NImECF(lbOdHO, PhpjBi) > LIKAgg) {
                return false;
            }
        };
        cnoMOg = Math.abs(Math.cos(hHgcCD) * NdGnPG);
        if (cnoMOg >= LIKAgg) {
            return false;
        };
        return true;
    };
    JpMdFf.prototype.FMGaPH = function (KEjEEl) {
        var ejDGcC = ggGkJc.oAcDfp(this.LcdpGp);
        if (this.BkoHcI.hPEEGo) {
            var pEmhPc = ggGkJc.KkjAMO()[2] * 0.5;
            if (ejDGcC[0] > pEmhPc) {
                ejDGcC[0] -= this.LcdpGp.offsetHeight;
            }
        };
        lJELmO.IFDeod(KEjEEl, ejDGcC);
        lJELmO.dMdbkN(KEjEEl, dDFAkd * (mKEgAF[0] / this.LcdpGp.offsetWidth));
        if (this.BkoHcI.hPEEGo) {
            var fOGnCG = KEjEEl[1];
            KEjEEl[1] = GdeJPB[1] - KEjEEl[0];
            KEjEEl[0] = fOGnCG;
        };
        lJELmO.BObpdE(KEjEEl);
    };
    JpMdFf.prototype.nbgJof = function (KEjEEl) {
        var ejDGcC = ggGkJc.oAcDfp(this.LcdpGp);
        if (this.BkoHcI.hPEEGo) {
            var pEmhPc = ggGkJc.KkjAMO()[2] * 0.5;
            if (ejDGcC[0] > pEmhPc) {
                ejDGcC[0] -= this.LcdpGp.offsetHeight;
            };
            var fOGnCG = KEjEEl[0];
            KEjEEl[0] = GdeJPB[1] - KEjEEl[1];
            KEjEEl[1] = fOGnCG;
        };
        lJELmO.HpDGlG(KEjEEl, dDFAkd * (mKEgAF[0] / this.LcdpGp.offsetWidth));
        lJELmO.jeDgdF(KEjEEl, ejDGcC);
        lJELmO.BObpdE(KEjEEl);
    };
    JpMdFf.prototype.DhcNbm = function (KEjEEl) {
        var ejDGcC = ggGkJc.oAcDfp(this.LcdpGp);
        lJELmO.HpDGlG(KEjEEl, dDFAkd * (mKEgAF[0] / this.LcdpGp.offsetWidth));
        lJELmO.jeDgdF(KEjEEl, ejDGcC);
        lJELmO.BObpdE(KEjEEl);
    };
    JpMdFf.prototype.eCMpjp = function (llChCG, nnIbMK) {
        if (this.GLJCMC >= CHfidh) {
            return;
        };
        this.GLJCMC++;
        nnIbMK = nnIbMK / this.pnkKjh;
        if (llChCG == 'OPKHjd') {
            if (nnIbMK > 0.7) {
                llChCG = 'ndNifi';
            } else if (nnIbMK > 0.3) {
                nnIbMK += 0.3;
                llChCG = 'BkOeel';
            } else {
                nnIbMK = nnIbMK * 2 + 0.2;
                llChCG = 'jFdnFM';
            }
        } else if (llChCG == 'NEeGOB') {
            nnIbMK += 0.2;
        } else if (llChCG == 'dchiKB') {
            if (nnIbMK < 0.2) {
                nnIbMK = 0.2;
            }
        };
        this.DpgGmk(llChCG, nnIbMK);
    };
    JpMdFf.prototype.DpgGmk = function (llChCG, DBmKAc) {
        var LJhpGD = AdnedG[llChCG];
        if (!LJhpGD) {
            $warn(llChCG);
            return;
        };
        if (DBmKAc > 0.85) {
            DBmKAc = 1;
        } else if (DBmKAc < 0.15) {
            return;
        };
        if (LJhpGD.length == 1) {
            JMBDGp.gDicAB(LJhpGD[0], DBmKAc, false, 0, false);
        } else {
            JMBDGp.gDicAB(LJhpGD.random(), DBmKAc, false, 0, false);
        }
    };
    return function () {
        return new eAeFAO(new JpMdFf(arguments))
    };
})();
BLAZE.NmiACa = NmiACa;
